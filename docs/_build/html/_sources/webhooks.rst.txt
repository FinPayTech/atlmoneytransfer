HTTP Notifications
==================

ATL Money Transfer can send HTTP Notifications that notify your application any time an event happens on your transaction. This is especially useful for events—like transaction paid or transaction payout failed. This mechanism is also useful for services that are not directly responsible for making an API request, but still need to know the response from that request.


The Notification Object
-----------------------

+---------------------------+-------------------------------------------------------------------------------------+
| Parameter                 | Description                                                                         |
+===========================+=====================================================================================+
| id                        | The transaction number on ATLMT Platform this notification belongs to.              |
+---------------------------+-------------------------------------------------------------------------------------+
| from_country              | The source country of transfer.                                                     |
+---------------------------+-------------------------------------------------------------------------------------+
| from_currency             | The source currency of transfer.                                                    |
+---------------------------+-------------------------------------------------------------------------------------+
| send_amount               | The source amount of transfer.                                                      |
+---------------------------+-------------------------------------------------------------------------------------+
| to_country                | The destination country of transfer.                                                |
+---------------------------+-------------------------------------------------------------------------------------+
| to_currency               | The payout currency of transfer.                                                    |
+---------------------------+-------------------------------------------------------------------------------------+
| payout_amount             | The payout amount of transfer.                                                      |
+---------------------------+-------------------------------------------------------------------------------------+
| payout_method             | The payout method for transfer.                                                     |
+---------------------------+-------------------------------------------------------------------------------------+
| exchange_rate             | Exchange rate applied ``from_currency`` to ``to_currency``.                         |
+---------------------------+-------------------------------------------------------------------------------------+
| fees                      | Transfer cost on partner's platform.                                                |
+---------------------------+-------------------------------------------------------------------------------------+
| settlement_currency       | Currency code which payout amount was settled with ATL Money Transfer.              |
+---------------------------+-------------------------------------------------------------------------------------+
| settlement_amount         | Payout amount converted from ``settlement_currency`` to ``to_currency``.            |
+---------------------------+-------------------------------------------------------------------------------------+
| commission                | ATL Money Transfer's Commission.                                                    |
+---------------------------+-------------------------------------------------------------------------------------+
| total_settlement          | Total settlement amount with ATL Money Transfer including commission.               |
+---------------------------+-------------------------------------------------------------------------------------+
| customer                  | Unique Identifier of customer.                                                      |
+---------------------------+-------------------------------------------------------------------------------------+
| recipient                 | Unique Identifier of recipient.                                                     |
+---------------------------+-------------------------------------------------------------------------------------+
| delivery_reference        | Collection PIN or Delivery Reference for the transfer.                              |
+---------------------------+-------------------------------------------------------------------------------------+
| third_party_reference     | Transaction reference on partner's platform.                                        |
+---------------------------+-------------------------------------------------------------------------------------+
| status                    | Transfer status for which notification was sent. See Transaction Statuses           |
+---------------------------+-------------------------------------------------------------------------------------+



Receiving HTTP Notifications with an HTTPS server
-------------------------------------------------

If you use an HTTPS URL for your HTTP Notification endpoint, ATL Money Transfer will validate that the connection to your server is secure before sending your notification data. For this to work, your server must be correctly configured to support HTTPS with a valid server certificate.


Responding to a HTTP Notifications
----------------------------------

To acknowledge receipt of a HTTP Notification, your endpoint should return a ``200`` HTTP status code. All response codes apart from this, including ``3xx`` codes, will indicate to ATL Money Transfer that you did not receive the HTTP Notification. This does mean that a URL redirection or a "Not Modified" response will be treated as a failure. ATL Money Transfer will ignore any other information returned in the request headers or request body.

In live mode, we will attempt to deliver your HTTP Notification for up to three days with an exponential back off. In test mode, we retry three times over a few hours. HTTP Notifications can be manually retried after this time, though you can query for the transaction to reconcile your data with any missed notifications.

When viewing a specific event information through the Dashboard, you can check how many times we've attempted to send an event to an endpoint by clicking on that endpoint URL in the HTTP Push Notifications section. This will show you the latest response we received from your endpoint, along with a number of attempted notifications and the respective HTTP status codes we received.

Best practices
--------------

Before going live, test that your HTTP Notification endpoint is working properly.

If your HTTP Notification endpoint script performs complex logic, or makes network calls, it's possible that the script would time out before ATL Money Transfer sees its complete execution. For that reason, you might want to have your HTTP Notification endpoint immediately acknowledge receipt by returning a ``200`` HTTP status code, and then perform the rest of its duties.

HTTP Notification endpoints might occasionally receive the same event more than once. We advise you to guard against duplicated event receipts by making your event processing idempotent. One way of doing this is logging the events you've processed, and then not processing already-logged events. Additionally, we recommend verifying HTTP Notification signatures to confirm that received events are being sent from ATL Money Transfer.


Notification Signatures
-----------------------

ATL Money Transfers signs all HTTP Notifications it sends to your endpoints. We do so by including a signature in each event’s ATLMoney-Signature header. This allows you to validate that the notification were sent by ATL Money Transfer, not by a third party. We recommend that you should always validate the signature of the notification.


Preventing replay attacks
-------------------------

A replay attack is when an attacker intercepts a valid payload and its signature, then re-transmits them. To mitigate such attacks, ATL Money Transfer includes a timestamp in the ATLMoney-Signature header. Because this timestamp is part of the signed payload, it is also verified by the signature, so an attacker cannot change the timestamp without invalidating the signature. If the signature is valid but the timestamp is too old, you can have your application reject the payload.

We recommend tolerance of five minutes between the timestamp and the current time. We also recommend that you use Network Time Protocol (NTP) to ensure that your server’s clock is accurate and synchronizes with the time on ATL Money Transfer's servers.

ATL Money Transfer generates the timestamp and signature each time we send a notification to your endpoint. If ATL Money Transfer retries an event (e.g., your endpoint previously replied with a non-200 status code), then we generate a new signature and timestamp for the new delivery attempt.


Verifying Signatures
--------------------

The ATLMoney-Signature header contains a timestamp and one or more signatures. The timestamp is prefixed by t=, and signature is prefixed by s=.

.. code-block:: console
  :linenos:

  ATLMoney-Signature: t=1492774577,
    s=123abcd456efgh789ijklmnopqrst

Note that newlines have been added in the example above for clarity, but a real ATLMoney-Signature header will be all one line.

ATL Money Transfer generates signatures using a hash-based message authentication code (HMAC) with SHA-256. To prevent downgrade attacks, you should ignore all schemes that are not s.

**Step 1: Extract the timestamp and signatures from the header**

Split the header, using the , character as the separator, to get a list of elements. Then split each element, using the = character as the separator, to get a prefix and value pair.

The value for the prefix t corresponds to the timestamp, and s corresponds to the signature. You can discard all other elements.

**Step 2: Prepare the payload_signature string**

You achieve this by concatenating:

- The timestamp (as a string)
- The character ``.``
- The actual JSON payload (i.e., the request’s body)

**Step 3: Determine the expected signature**

Compute an HMAC with the SHA256 hash function. Use the endpoint’s signing secret as the key, and use the payload_signature string as the message.

**Step 4: Compare signatures**

Compare the signature in the header to the expected signature. If a signature matches, compute the difference between the current timestamp and the received timestamp, then decide if the difference is within your tolerance.

To protect against timing attacks, use a constant-time string comparison to compare the expected signature to each of the received signatures.
