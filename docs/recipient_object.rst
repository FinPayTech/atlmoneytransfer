Recipient Object
================

The recipient object varies for each corridor and payout method.

+------------------------------+------------------------------------------------------------------------------+
| Parameter                    | Description                                                                  |
+==============================+==============================================================================+
| id                           | Unique Identification Number for recipient on ATL Money Transfer platform.   |
+------------------------------+------------------------------------------------------------------------------+
| full_name                    | Full name of the recipient.                                                  |
+------------------------------+------------------------------------------------------------------------------+
| type                         | IND for Individual Recipient and BIZ for Business Recipient.                 |
+------------------------------+------------------------------------------------------------------------------+
| payout_method                | Payout method for the recipient.                                             |
+------------------------------+------------------------------------------------------------------------------+
| country                      | Country of the recipient.                                                    |
+------------------------------+------------------------------------------------------------------------------+
| param_1                      | Please see Country Payout Configuration.                                     |
+------------------------------+------------------------------------------------------------------------------+
| param_2                      | Please see Country Payout Configuration.                                     |
+------------------------------+------------------------------------------------------------------------------+
| param_n                      | Please see Country Payout Configuration.                                     |
+------------------------------+------------------------------------------------------------------------------+
| relation                     | Relation with recipient. See Resources > Relation Types                      |
+------------------------------+------------------------------------------------------------------------------+
| created_on                   | Date when the recipient record was created.                                  |
+------------------------------+------------------------------------------------------------------------------+
| updated_on                   | Date when the recipient record was last modified.                            |
+------------------------------+------------------------------------------------------------------------------+

.. NOTE::
  Please review **Country Payout Configuration** for replacement of parameters starting with ``param_``.

Creating New Recipient
----------------------

Create a new recipient under a customer.

Endpoint: ``https://www.atlmoneytransfer.com/api/recipients``

Method: ``POST``

+---------------------+------------+-------------------------------------------------------------------------+
| Parameter           | Mandatory  | Description                                                             |
+=====================+============+=========================================================================+
| customer            | Yes        | Unique ID of customer the recipient belongs to.                         |
+---------------------+------------+-------------------------------------------------------------------------+
| type                | Yes        | IND for Individual Recipient and BIZ for Business Recipient.            |
+---------------------+------------+-------------------------------------------------------------------------+
| country             | Yes        | Country code of destination.                                            |
+---------------------+------------+-------------------------------------------------------------------------+
| payout_method       | Yes        | Payout method code for recipient.                                       |
+---------------------+------------+-------------------------------------------------------------------------+
| relation            | No         | Relation with recipient. See Resources > Relation Types                 |
+---------------------+------------+-------------------------------------------------------------------------+

.. HINT::
   Since a resource is being created, HTTP response code ``201`` will be returned if the recipient is successfully created.


**Eg. Creating an Individual recipient for Bank Transfer in Austria**

.. code-block:: console

  POST /api/recipients HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx
  Content-Type: application/x-www-form-urlencoded

  customer=9963210701
  &type=IND
  &country=AT
  &payout_method=AC
  &first_name=Richard
  &last_name=AMOAH
  &bank=American+Express+Bank+Ltd
  &iban=AT611904300234573201
  &mobile_number=
  &relation=BIZ

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "recipient": {
          "id": 9221768696,
          "full_name": "Richard AMOAH",
          "type": "IND",
          "payout_method": "AC",
          "country": "AT",
          "customer": 9963210701,
          "first_name": "Richard",
          "iban": "AT611904300234573201",
          "last_name": "AMOAH",
          "bank": "American Express Bank Ltd",
          "mobile_number": "",
          "relation": "BIZ",
          "created_on": "2018-09-29T13:16:52+00:00",
          "updated_on": "2018-09-29T13:16:52+00:00"
      }
  }

Get all Recipients
------------------

Get all recipients for a customer.

Endpoint: ``https://www.atlmoneytransfer.com/api/recipients/:customerId``

Method: ``POST``

+-----------------------+------------------+-----------------------------------------------------------+
| Param                 | Mandatory        | Description                                               |
+=======================+==================+===========================================================+
| page                  | No               | Page number of result set.                                |
+-----------------------+------------------+-----------------------------------------------------------+

**Request**

.. code-block:: console

  GET /api/recipients/9963210701 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "recipients": [
        {
            "id": 2665701193,
            "full_name": "AGPAYTECH Ltd",
            "type": "BIZ",
            "payout_method": "AC",
            "country": "AT",
            "customer": 9963210701,
            "iban": "AT611904300234573201",
            "business_name": "AGPAYTECH Ltd",
            "mobile_number": "",
            "bank": "American Express Bank Ltd",
            "relation": "BIZ",
            "created_on": "2018-09-29T13:26:35+00:00",
            "updated_on": "2018-09-29T13:26:35+00:00"
        },
        {
            "id": 9221768696,
            "full_name": "Richard AMOAH",
            "type": "IND",
            "payout_method": "AC",
            "country": "AT",
            "customer": 9963210701,
            "first_name": "Richard",
            "iban": "AT611904300234573201",
            "last_name": "AMOAH",
            "bank": "American Express Bank Ltd",
            "mobile_number": "",
            "relation": "BIZ",
            "created_on": "2018-09-29T13:16:52+00:00",
            "updated_on": "2018-09-29T13:16:52+00:00"
        }
    ],
    "current_recipients": 2,
    "total_recipients": 2,
    "page": 1,
    "total_pages": 1
  }

Get Single Recipient
--------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/recipient/:recipientId``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/recipient/2665701193 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "recipient": {
        "id": 2665701193,
        "full_name": "AGPAYTECH Ltd",
        "type": "BIZ",
        "payout_method": "AC",
        "country": "AT",
        "customer": 9963210701,
        "iban": "AT611904300234573201",
        "business_name": "AGPAYTECH Ltd",
        "mobile_number": "",
        "bank": "American Express Bank Ltd",
        "relation": "BIZ",
        "created_on": "2018-09-29T13:26:35+00:00",
        "updated_on": "2018-09-29T13:26:35+00:00"
    }
  }

Update Recipient
----------------

Endpoint: ``https://www.atlmoneytransfer.com/api/recipient/:recipientId``

Method: ``POST``

**Request**

.. code-block:: console

  POST /api/recipient/2665701193 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx
  Content-Type: application/x-www-form-urlencoded

  iban=AT611904300234573202
  &bank=Deutsche+Bank

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "recipient": {
        "id": 2665701193,
        "full_name": "AGPAYTECH Ltd",
        "type": "BIZ",
        "payout_method": "AC",
        "country": "AT",
        "customer": 9963210701,
        "iban": "AT611904300234573202",
        "business_name": "AGPAYTECH Ltd",
        "mobile_number": "",
        "bank": "Deutsche Bank",
        "relation": "BIZ",
        "created_on": "2018-09-29T13:26:35+00:00",
        "updated_on": "2018-09-29T13:58:49+00:00"
    }
  }
