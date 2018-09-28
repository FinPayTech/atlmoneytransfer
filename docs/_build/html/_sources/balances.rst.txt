Balance
=======

Endpoint: ``https://www.atlmoneytransfer.com/api/balances``

Method: ``GET``

Get balance in all currencies
-----------------------------

**Request**

.. code-block:: console

  GET /api/balances HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "balances": {
        "GBP": "5000.00",
        "EUR": "10000.00"
    }
  }

Get balance for specific currency
---------------------------------

**Request**

.. code-block:: console

  GET /api/balances/GBP HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "balance": "5000.00"
  }

Account Statement
-----------------

Endpoint: ``https://www.atlmoneytransfer.com/api/statement/:currency``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------+
| Param                 | Mandatory        | Description                                               |
+=======================+==================+===========================================================+
| page                  | No               | Page number of result set.                                |
+-----------------------+------------------+-----------------------------------------------------------+
| start                 | No               | Start date of statement in YYYY-MM-DD format              |
+-----------------------+------------------+-----------------------------------------------------------+
| end                   | No               | End date of statement in YYYY-MM-DD format.               |
+-----------------------+------------------+-----------------------------------------------------------+

**Request**

.. code-block:: console

  GET /api/statement/GBP HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "entries": [
        {
            "id": "04341ac2-6304-4ad4-9e13-fd4ba7575f2e",
            "transaction_number": "",
            "delivery_reference": "",
            "narration": "Initial Funding",
            "amount": "5000.00",
            "commission": "0.00",
            "created": "2018-09-19T14:19:16+00:00"
        }
    ],
    "current_entries": 1,
    "total_entries": 1,
    "page": 1,
    "total_pages": 1
  }

**Response Description**

+-------------------------------------+------------------------------------------------------------------+
| Field                               | Description                                                      |
+=====================================+==================================================================+
| entries.{n}.id                      | Unique Identifier for statement record.                          |
+-------------------------------------+------------------------------------------------------------------+
| entries.{n}.transaction_number      | Transaction number on ATL Money Transfer Platform                |
+-------------------------------------+------------------------------------------------------------------+
| entries.{n}.delivery_reference      | Delivery reference or collection pin for transaction.            |
+-------------------------------------+------------------------------------------------------------------+
| entries.{n}.narration               | Narration for statement record.                                  |
+-------------------------------------+------------------------------------------------------------------+
| entries.{n}.amount                  | Amount involved in operation.                                    |
+-------------------------------------+------------------------------------------------------------------+
| entries.{n}.commission              | ATL Money Transfer's commission.                                 |
+-------------------------------------+------------------------------------------------------------------+
| entries.{n}.created                 | Record creation date.                                            |
+-------------------------------------+------------------------------------------------------------------+
