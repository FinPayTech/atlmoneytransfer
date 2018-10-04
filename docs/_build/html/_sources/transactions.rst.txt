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
| created_on                   | Date when transaction was created on ATL Money Transfer's Platform.                 |
+------------------------------+-------------------------------------------------------------------------------------+

Sending New Transaction
-----------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/transactions``

Method: ``POST``

+------------------------------+-------------------------------------------------------------------------------------+
| Parameter                    | Description                                                                         |
+==============================+=====================================================================================+
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


.. HINT::
   Since a resource is being created, HTTP response code ``201`` will be returned if the transaction is successfully created.


**Request**

.. code-block:: console

  POST /api/transactions HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx
  Content-Type: application/x-www-form-urlencoded

  from_country=GB
  &from_currency=GBP
  &send_amount=4000
  &to_country=SL
  &to_currency=SLL
  &payout_amount=41600000
  &payout_method=CP
  &payout_partner=BCXSL
  &exchange_rate=10400
  &fees=200
  &third_party_reference=K00001
  &customer%5Bfirst_name%5D=James
  &customer%5Bmiddle_name%5D=
  &customer%5Blast_name%5D=Anderson
  &customer%5Bdate_of_birth%5D=1990-01-01
  &customer%5Bbirth_city%5D=London
  &customer%5Bbirth_country%5D=GB
  &customer%5Bnationality%5D=GB
  &customer%5Bbirth_nationality%5D=GB
  &customer%5Baddress%5D=128+Peckham+Hill+Street
  &customer%5Bcity%5D=London
  &customer%5Bregion%5D=England
  &customer%5Bpostcode%5D=SE15+5JT
  &customer%5Bcountry%5D=GB
  &customer%5Bphone_number%5D=1234567890
  &customer%5Bmobile_number%5D=9876543210&
  customer%5Bemail_address%5D=support%40atlmoneytransfer.com
  &recipient%5Btype%5D=IND
  &recipient%5Bfirst_name%5D=Maria
  &recipient%5Blast_name%5D=Anderson
  &recipient%5Baddress%5D=50+Siaka+Stevens+Street
  &recipient%5Bcity%5D=Freetown
  &recipient%5Bregion%5D=
  &recipient%5Bpostcode%5D=
  &recipient%5Bmobile_number%5D=147852369
  &recipient%5Bemail%5D=support%40atlmoneytransfer.com
  &recipient%5Brelation%5D=FAM
  &purpose=FS
  &message=Happy+Birthday

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "transaction": {
        "id": "88800002",
        "from_country": "GB",
        "from_currency": "GBP",
        "send_amount": 4000,
        "to_country": "SL",
        "to_currency": "SLL",
        "payout_amount": 41600000,
        "payout_method": "CP",
        "payout_partner": "BCXSL",
        "exchange_rate": "10400.000000",
        "fees": 200,
        "settlement_currency": "GBP",
        "settlement_amount": 3961.9,
        "commission": 39.62,
        "total_settlement": 4001.52,
        "delivery_reference": 12855396338,
        "third_party_reference": "K00001",
        "customer": {
            "id": 9010307060,
            "first_name": "James",
            "middle_name": "",
            "last_name": "Anderson",
            "date_of_birth": "1990-01-01",
            "birth_city": "London",
            "birth_country": "GB",
            "nationality": "GB",
            "birth_nationality": "GB",
            "address": "128 Peckham Hill Street",
            "city": "London",
            "region": "England",
            "postcode": "SE15 5JT",
            "country": "GB",
            "mobile_number": "9876543210",
            "phone_number": "1234567890",
            "email_address": "support@atlmoneytransfer.com"
        },
        "recipient": {
            "id": 5109069783,
            "full_name": "Maria Anderson",
            "type": "IND",
            "first_name": "Maria",
            "last_name": "Anderson",
            "mobile_number": "147852369",
            "address": "50 Siaka Stevens Street",
            "city": "Freetown",
            "region": "",
            "postcode": "",
            "email": "support@atlmoneytransfer.com",
            "relation": "FAM"
        },
        "status": "AVAILABLE",
        "purpose": "FS",
        "message": "Happy Birthday",
        "created_on": "2018-10-04T12:29:24+00:00"
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
              "send_amount": 4000,
              "to_country": "SL",
              "to_currency": "SLL",
              "payout_amount": 41600000,
              "payout_method": "CP",
              "payout_partner": "BCXSL",
              "exchange_rate": "10400.000000",
              "fees": 200,
              "settlement_currency": "GBP",
              "settlement_amount": 3961.9,
              "commission": 39.62,
              "total_settlement": 4001.52,
              "delivery_reference": 12864909190,
              "third_party_reference": "K00001",
              "status": "AVAILABLE",
              "created_on": "2018-10-04T12:21:21+00:00"
          },
          {
              "id": "88800002",
              "from_country": "GB",
              "from_currency": "GBP",
              "send_amount": 4000,
              "to_country": "SL",
              "to_currency": "SLL",
              "payout_amount": 41600000,
              "payout_method": "CP",
              "payout_partner": "BCXSL",
              "exchange_rate": "10400.000000",
              "fees": 200,
              "settlement_currency": "GBP",
              "settlement_amount": 3961.9,
              "commission": 39.62,
              "total_settlement": 4001.52,
              "delivery_reference": 12855396338,
              "third_party_reference": "K00001",
              "status": "AVAILABLE",
              "created_on": "2018-10-04T12:29:24+00:00"
          }
      ],
      "current_transactions": 2,
      "total_transactions": 2,
      "page": 1,
      "total_pages": 1
  }



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
