Resources
=========

Get list of Countries
---------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/resources/countries``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/resources/countries HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "countries": [
          {
              "code": "AF",
              "title": "Afghanistan",
              "currency": "AFN"
          },
          {
              "code": "AL",
              "title": "Albania",
              "currency": "ALL"
          },
          {
              "code": "DZ",
              "title": "Algeria",
              "currency": "DZD"
          },
          {
              "code": "AS",
              "title": "American Samoa",
              "currency": "USD"
          },
          {
              "code": "AD",
              "title": "Andorra",
              "currency": "EUR"
          },
          {
              "code": "AO",
              "title": "Angola",
              "currency": "AOA"
          }
      ]
  }

Get list of Currencies
----------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/resources/currencies``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/resources/currencies HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "currencies": [
        {
            "code": "AFN",
            "title": "Afghan afghani"
        },
        {
            "code": "ALL",
            "title": "Albanian lek"
        },
        {
            "code": "DZD",
            "title": "Algerian dinar"
        },
        {
            "code": "AOA",
            "title": "Angolan kwanza"
        },
        {
            "code": "ARS",
            "title": "Argentine peso"
        },
        {
            "code": "AMD",
            "title": "Armenian dram"
        },
        {
            "code": "AWG",
            "title": "Aruban florin"
        },
        {
            "code": "AUD",
            "title": "Australian dollar"
        }
    ]
  }

Validate mobile number for Instant Pay in Ghana
-----------------------------------------------

Validate account number for Instant Pay in Ghana
------------------------------------------------
