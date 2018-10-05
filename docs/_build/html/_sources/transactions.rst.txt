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
| poi_document                 | Document of the uploaded Proof of ID (POI). Eg. PAS or DRV etc.                     |
+------------------------------+-------------------------------------------------------------------------------------+
| poi_id_number                | Document ID Number of uploaded POI.                                                 |
+------------------------------+-------------------------------------------------------------------------------------+
| poi_valid_from               | Document valid from date of the uploaded POI.                                       |
+------------------------------+-------------------------------------------------------------------------------------+
| poi_expiry                   | Document expiry date of the uploaded POI.                                           |
+------------------------------+-------------------------------------------------------------------------------------+
| status                       | Current transaction status. See Transaction Statuses                                |
+------------------------------+-------------------------------------------------------------------------------------+
| created_on                   | Date when transaction was created on ATL Money Transfer's Platform.                 |
+------------------------------+-------------------------------------------------------------------------------------+

Sending New Transaction
-----------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/transactions``

Method: ``POST``

+------------------------------+-------------+-------------------------------------------------------------------------+
| Parameter                    | Mandatory   | Description                                                             |
+==============================+=============+=========================================================================+
| from_country                 | Yes         | The source country of transfer.                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| from_currency                | Yes         | The source currency of transfer.                                        |
+------------------------------+-------------+-------------------------------------------------------------------------+
| send_amount                  | Yes         | The source amount of transfer.                                          |
+------------------------------+-------------+-------------------------------------------------------------------------+
| to_country                   | Yes         | The destination country of transfer.                                    |
+------------------------------+-------------+-------------------------------------------------------------------------+
| to_currency                  | Yes         | The payout currency of transfer.                                        |
+------------------------------+-------------+-------------------------------------------------------------------------+
| payout_amount                | Yes         | The payout amount of transfer.                                          |
+------------------------------+-------------+-------------------------------------------------------------------------+
| payout_method                | Yes         | The payout method for transfer.                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| payout_partner               | Conditional | The payout partner for Cash Pickup transfers.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| exchange_rate                | Yes         | Exchange rate applied ``from_currency`` to ``to_currency``.             |
+------------------------------+-------------+-------------------------------------------------------------------------+
| fees                         | Yes         | Transfer cost on partner's platform.                                    |
+------------------------------+-------------+-------------------------------------------------------------------------+
| third_party_reference        | Yes         | Transaction reference on partner's platform.                            |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[id]                 | No          | Customer Unique Identifier on ATL Money Transfer.                       |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[first_name]         | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[middle_name]        | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[last_name]          | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[date_of_birth]      | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[birth_city]         | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[birth_country]      | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[nationality]        | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[birth_nationality]  | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[address]            | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[city]               | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[region]             | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[postcode]           | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[country]            | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[phone_number]       | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[mobile_number]      | Conditional | Required if ``customer[id]`` is not provided.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| customer[email_address]      | No          |                                                                         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| recipient[id]                | No          | Unique Identification Number for recipient on ATLMT.                    |
+------------------------------+-------------+-------------------------------------------------------------------------+
| recipient[type]              | Conditional | Required if ``recipient[id]`` is not provided.                          |
+------------------------------+-------------+-------------------------------------------------------------------------+
| recipient[param_1]           | Conditional | Optional if ``recipient[id]`` is provided.                              |
+------------------------------+-------------+-------------------------------------------------------------------------+
| recipient[param_2]           | Conditional | Optional if ``recipient[id]`` is provided.                              |
+------------------------------+-------------+-------------------------------------------------------------------------+
| recipient[param_n]           | Conditional | Optional if ``recipient[id]`` is provided.                              |
+------------------------------+-------------+-------------------------------------------------------------------------+
| recipient[relation]          | Conditional | Optional if ``recipient[id]`` is provided.                              |
+------------------------------+-------------+-------------------------------------------------------------------------+
| purpose                      | Yes         | Purpose code of the transfer.                                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| message                      | No          | Message for recipient. If any                                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| poi_document                 | Conditional | Document of the uploaded Proof of ID (POI). Eg. PAS or DRV etc.         |
+------------------------------+-------------+-------------------------------------------------------------------------+
| poi_id_number                | Conditional | Document ID Number of uploaded POI.                                     |
+------------------------------+-------------+-------------------------------------------------------------------------+
| poi_valid_from               | Conditional | Document valid from date of the uploaded POI.                           |
+------------------------------+-------------+-------------------------------------------------------------------------+
| poi_expiry                   | Conditional | Document expiry date of the uploaded POI.                               |
+------------------------------+-------------+-------------------------------------------------------------------------+
| poi_file                     | Conditional | File to be uploaded. Only images and pdf are accepted.                  |
+------------------------------+-------------+-------------------------------------------------------------------------+


.. HINT::
   Since a resource is being created, HTTP response code ``201`` will be returned if the transaction is successfully created.

.. WARNING::
   Since sending new transfer require necessary network calls to various payout partners we recommend that you set a minimum **150 seconds** as request time-out value for your HTTP Client.

**Request**

.. code-block:: console
  :linenos:

  curl -X POST \
  https://www.atlmoneytransfer.com/api/transactions \
  -H 'Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx' \
  -F from_country=GB \
  -F from_currency=GBP \
  -F send_amount=500 \
  -F to_country=SL \
  -F to_currency=SLL \
  -F payout_amount=5000000 \
  -F payout_method=CP \
  -F payout_partner=BCXSL \
  -F exchange_rate=10000 \
  -F fees=20 \
  -F purpose=INVST \
  -F 'message=Invoice Payment #100001' \
  -F 'customer[first_name]=John' \
  -F 'customer[last_name]=Doe' \
  -F 'customer[date_of_birth]=1980-09-01' \
  -F 'customer[nationality]=GB' \
  -F 'customer[birth_nationality]=GB' \
  -F 'customer[birth_city]=London' \
  -F 'customer[birth_country]=GB' \
  -F 'customer[address]=128 Peckham Hill Street' \
  -F 'customer[city]=London' \
  -F 'customer[region]=England' \
  -F 'customer[postcode]=SE15 5JT' \
  -F 'customer[country]=GB' \
  -F 'customer[mobile_number]=1234567890' \
  -F 'customer[email]=support@atlmoneytransfer.com' \
  -F poi_document=PAS \
  -F poi_id_number=P12345678 \
  -F poi_valid_from=2008-10-06 \
  -F poi_expiry=2018-10-05 \
  -F poi_file=@/home/appdevd/Downloads/Passport.jpg \
  -F 'recipient[type]=IND' \
  -F 'recipient[relation]=BIZ' \
  -F 'recipient[first_name]=Richard' \
  -F 'recipient[last_name]=AMOAH' \
  -F 'recipient[address]=Freetown' \
  -F 'recipient[city]=Freetown' \
  -F 'recipient[region]=Freetown' \
  -F 'recipient[mobile_number]=123456789' \
  -F third_party_reference=K00001

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "transaction": {
        "id": "88800001",
        "from_country": "GB",
        "from_currency": "GBP",
        "send_amount": 500,
        "to_country": "SL",
        "to_currency": "SLL",
        "payout_amount": 5000000,
        "payout_method": "CP",
        "payout_partner": "BCXSL",
        "exchange_rate": "10000.000000",
        "fees": 20,
        "settlement_currency": "GBP",
        "settlement_amount": 476.19,
        "commission": 4.76,
        "total_settlement": 480.95,
        "delivery_reference": 12879511712,
        "third_party_reference": "K00001",
        "customer": {
            "id": 7209673523,
            "first_name": "John",
            "middle_name": null,
            "last_name": "Doe",
            "date_of_birth": "1980-09-01",
            "birth_city": "London",
            "birth_country": "GB",
            "nationality": "GB",
            "birth_nationality": "GB",
            "address": "128 Peckham Hill Street",
            "city": "London",
            "region": "England",
            "postcode": "SE15 5JT",
            "country": "GB",
            "mobile_number": "1234567890",
            "phone_number": null,
            "email_address": null
        },
        "recipient": {
            "id": 2531137994,
            "full_name": "Richard AMOAH",
            "type": "IND",
            "first_name": "Richard",
            "last_name": "AMOAH",
            "mobile_number": "123456789",
            "address": "Freetown",
            "city": "Freetown",
            "region": "Freetown",
            "postcode": null,
            "email": null,
            "relation": "BIZ"
        },
        "status": "HOLD",
        "purpose": "INVST",
        "poi_document": "PAS",
        "poi_id_number": "P12345678",
        "poi_valid_from": "2008-10-06",
        "poi_expiry": "2018-10-05",
        "message": "Invoice Payment #100001",
        "created_on": "2018-10-05T10:43:33+00:00"
    }
  }

Get all Transactions
--------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/transactions``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------+
| Param                 | Mandatory        | Description                                               |
+=======================+==================+===========================================================+
| page                  | No               | Page number of result set.                                |
+-----------------------+------------------+-----------------------------------------------------------+
| start                 | No               | Start date for filtering records in YYYY-MM-DD format.    |
+-----------------------+------------------+-----------------------------------------------------------+
| end                   | No               | End date for filtering records in YYYY-MM-DD format.      |
+-----------------------+------------------+-----------------------------------------------------------+


**Request**

.. code-block:: console

  GET /api/transactions HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "transactions": [
        {
            "id": "88800001",
            "from_country": "GB",
            "from_currency": "GBP",
            "send_amount": 500,
            "to_country": "SL",
            "to_currency": "SLL",
            "payout_amount": 5000000,
            "payout_method": "CP",
            "payout_partner": "BCXSL",
            "exchange_rate": "10000.000000",
            "fees": 20,
            "settlement_currency": "GBP",
            "settlement_amount": 476.19,
            "commission": 4.76,
            "total_settlement": 480.95,
            "delivery_reference": 12879511712,
            "third_party_reference": "K00001",
            "status": "HOLD",
            "created_on": "2018-10-05T10:43:33+00:00"
        }
    ],
    "current_transactions": 1,
    "total_transactions": 1,
    "page": 1,
    "total_pages": 1
  }



Get Single Transaction
----------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/transactions/:id``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/transactions/88800001 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx


**Response**

.. code-block:: JSON

  {
    "message": "success",
    "transaction": {
        "id": "88800001",
        "from_country": "GB",
        "from_currency": "GBP",
        "send_amount": 500,
        "to_country": "SL",
        "to_currency": "SLL",
        "payout_amount": 5000000,
        "payout_method": "CP",
        "payout_partner": "BCXSL",
        "exchange_rate": "10000.000000",
        "fees": 20,
        "settlement_currency": "GBP",
        "settlement_amount": 476.19,
        "commission": 4.76,
        "total_settlement": 480.95,
        "delivery_reference": 12879511712,
        "third_party_reference": "K00001",
        "customer": {
            "id": 7209673523,
            "first_name": "John",
            "middle_name": null,
            "last_name": "Doe",
            "date_of_birth": "1980-09-01",
            "birth_city": "London",
            "birth_country": "GB",
            "nationality": "GB",
            "birth_nationality": "GB",
            "address": "128 Peckham Hill Street",
            "city": "London",
            "region": "England",
            "postcode": "SE15 5JT",
            "country": "GB",
            "mobile_number": "1234567890",
            "phone_number": null,
            "email_address": null
        },
        "recipient": {
            "id": 2531137994,
            "full_name": "Richard AMOAH",
            "type": "IND",
            "first_name": "Richard",
            "last_name": "AMOAH",
            "mobile_number": "123456789",
            "address": "Freetown",
            "city": "Freetown",
            "region": "Freetown",
            "postcode": null,
            "email": null,
            "relation": "BIZ"
        },
        "status": "HOLD",
        "purpose": "INVST",
        "poi_document": "PAS",
        "poi_id_number": "P12345678",
        "poi_valid_from": "2008-10-06",
        "poi_expiry": "2018-10-05",
        "message": "Invoice Payment #100001",
        "created_on": "2018-10-05T10:43:33+00:00"
    }
  }

Cancel Transaction
------------------

Endpoint:

Method:

**Request**

**Response**
