Transactions
============

Transaction Object
------------------

+------------------------------+-------------------------------------------------------------------------------------+
| Parameter                    | Description                                                                         |
+==============================+=====================================================================================+
| id                           | The transaction number on ATLMT Platform.                                           |
+------------------------------+-------------------------------------------------------------------------------------+
| from_country                 | The source country of transfer.                                                     |
+------------------------------+-------------------------------------------------------------------------------------+
| from_currency                | The source currency of transfer.                                                    |
+------------------------------+-------------------------------------------------------------------------------------+
| send_amount                  | The source amount of transfer.                                                      |
+------------------------------+-------------------------------------------------------------------------------------+
| to_country                   | The destination country of transfer.                                                |
+------------------------------+-------------------------------------------------------------------------------------+
| to_currency                  | The payout currency of transfer.                                                    |
+------------------------------+-------------------------------------------------------------------------------------+
| payout_amount                | The payout amount of transfer.                                                      |
+------------------------------+-------------------------------------------------------------------------------------+
| payout_method                | The payout method for transfer.                                                     |
+------------------------------+-------------------------------------------------------------------------------------+
| payout_partner               | The payout partner for Cash Pickup transfers.                                       |
+------------------------------+-------------------------------------------------------------------------------------+
| exchange_rate                | Exchange rate applied ``from_currency`` to ``to_currency``.                         |
+------------------------------+-------------------------------------------------------------------------------------+
| fees                         | Transfer cost on partner's platform.                                                |
+------------------------------+-------------------------------------------------------------------------------------+
| settlement_currency          | Currency code which payout amount was settled with ATL Money Transfer.              |
+------------------------------+-------------------------------------------------------------------------------------+
| settlement_amount            | Payout amount converted from ``settlement_currency`` to ``to_currency``.            |
+------------------------------+-------------------------------------------------------------------------------------+
| commission                   | ATL Money Transfer's Commission.                                                    |
+------------------------------+-------------------------------------------------------------------------------------+
| total_settlement             | Total settlement amount with ATL Money Transfer including commission.               |
+------------------------------+-------------------------------------------------------------------------------------+
| delivery_reference           | Collection PIN or Delivery Reference for the transfer.                              |
+------------------------------+-------------------------------------------------------------------------------------+
| third_party_reference        | Transaction reference on partner's platform.                                        |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.id                  | Global unique identifier for customer.                                              |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.first_name          | First name of the customer this transaction belongs to.                             |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.middle_name         | Middle name of the customer this transaction belongs to.                            |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.last_name           | Last name of the customer this transaction belongs to.                              |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.date_of_birth       | Date of birth of the customer.                                                      |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.birth_city          | Birth city of the customer.                                                         |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.birth_country       | Birth country of the customer.                                                      |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.nationality         | Current nationality of the customer.                                                |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.birth_nationality   | Nationality of the customer at the time of birth.                                   |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.address             | Address of the customer.                                                            |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.city                | City where the customer is located.                                                 |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.region              | State/Province/Region where the customer is located.                                |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.postcode            | Postcode of the area where the customer is located.                                 |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.country             | Country where the customer is located.                                              |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.phone_number        | Phone number of the customer.                                                       |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.mobile_number       | Mobile number of the customer.                                                      |
+------------------------------+-------------------------------------------------------------------------------------+
| customer.email_address       | Email address of the customer.                                                      |
+------------------------------+-------------------------------------------------------------------------------------+
| recipient.id                 | Unique Identification Number for recipient on ATLMT.                                |
+------------------------------+-------------------------------------------------------------------------------------+
| recipient.full_name          | Full name of the recipient.                                                         |
+------------------------------+-------------------------------------------------------------------------------------+
| recipient.type               | IND for Individual Recipient and BIZ for Business Recipient.                        |
+------------------------------+-------------------------------------------------------------------------------------+
| recipient.param_1            | Please see Country Payout Configuration.                                            |
+------------------------------+-------------------------------------------------------------------------------------+
| recipient.param_2            | Please see Country Payout Configuration.                                            |
+------------------------------+-------------------------------------------------------------------------------------+
| recipient.param_n            | Please see Country Payout Configuration.                                            |
+------------------------------+-------------------------------------------------------------------------------------+
| recipient.relation           | Relation with recipient. See Resources > Relation Types                             |
+------------------------------+-------------------------------------------------------------------------------------+
| purpose                      | Purpose code of the transfer.                                                       |
+------------------------------+-------------------------------------------------------------------------------------+
| message                      | Message for recipient. If any                                                       |
+------------------------------+-------------------------------------------------------------------------------------+
| status                       | Current transaction status. See Transaction Statuses                                |
+------------------------------+-------------------------------------------------------------------------------------+
| environment                  | ``live`` or ``sandbox`` according to environment used for transaction.              |
+------------------------------+-------------------------------------------------------------------------------------+

Sending New Transaction
-----------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/transactions``

Method: ``POST``

**Request**

.. code-block:: console

  POST /api/transactions HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx
  Content-Type: application/x-www-form-urlencoded

**Response**

Get all Transactions
--------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/transactions``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/transactions HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**



Get Single Transaction
----------------------

Endpoint:

Method:

**Request**

**Response**

Cancel Transaction
------------------

Endpoint:

Method:

**Request**

**Response**
