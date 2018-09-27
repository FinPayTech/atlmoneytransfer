Settlement Rates
================

Endpoint: ``https://www.atlmoneytransfer.com/api/settlement-rates``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/settlement-rates HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "rates": [
          {
              "from": "GBP",
              "to": "CAD",
              "rate": 1.703422
          },
          {
              "from": "GBP",
              "to": "DKK",
              "rate": 8.328481
          },
          {
              "from": "GBP",
              "to": "EUR",
              "rate": 1.116487
          },
          {
              "from": "GBP",
              "to": "GHS",
              "rate": 6.42274
          },
          {
              "from": "GBP",
              "to": "NGN",
              "rate": 455
          },
          {
              "from": "GBP",
              "to": "SLL",
              "rate": 10500
          },
          {
              "from": "GBP",
              "to": "USD",
              "rate": 1.313538
          },
          {
              "from": "GBP",
              "to": "XAF",
              "rate": 730
          },
          {
              "from": "GBP",
              "to": "XOF",
              "rate": 730
          }
      ]
  }
