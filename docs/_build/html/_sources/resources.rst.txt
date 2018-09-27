Resources
=========

KYC Document Types
------------------

+-----------------+-------------------------------------------------------+
| Code            | Description                                           |
+=================+=======================================================+
| POI             | Proof of Identity                                     |
+-----------------+-------------------------------------------------------+
| POA             | Proof of Address                                      |
+-----------------+-------------------------------------------------------+
| SOF             | Source of Funds                                       |
+-----------------+-------------------------------------------------------+


Accepted KYC Documents
----------------------

+-----------------+------------------------+-------------------------------------------------------+
| Code            | Categories             | Description                                           |
+=================+========================+=======================================================+
| PAS             | POI                    | Passport                                              |
+-----------------+------------------------+-------------------------------------------------------+
| DRV             | POI                    | Driving License                                       |
+-----------------+------------------------+-------------------------------------------------------+
| EU              | POI                    | EU National ID                                        |
+-----------------+------------------------+-------------------------------------------------------+
| VID             | POI                    | Voter Card                                            |
+-----------------+------------------------+-------------------------------------------------------+
| COC             | POI                    | Consular Card                                         |
+-----------------+------------------------+-------------------------------------------------------+
| DIP             | POI                    | Diplomatic Card                                       |
+-----------------+------------------------+-------------------------------------------------------+
| NNL             | POI                    | National Identity Card                                |
+-----------------+------------------------+-------------------------------------------------------+
| BAC             | POA & SOF              | Bank Statement                                        |
+-----------------+------------------------+-------------------------------------------------------+
| GAS             | POA                    | Gas Bill                                              |
+-----------------+------------------------+-------------------------------------------------------+
| ELE             | POA                    | Electricity Bill                                      |
+-----------------+------------------------+-------------------------------------------------------+
| LLB             | POA                    | Landline Bill                                         |
+-----------------+------------------------+-------------------------------------------------------+
| TAX             | SOF                    | Tax Document                                          |
+-----------------+------------------------+-------------------------------------------------------+
| LC              | SOF                    | Loan Contract                                         |
+-----------------+------------------------+-------------------------------------------------------+
| P60             | SOF                    | P60 Document                                          |
+-----------------+------------------------+-------------------------------------------------------+


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

Get list of Nationalities
-------------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/resources/nationalities``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/resources/nationalities HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "nationalities": [
        {
            "code": "AF",
            "title": "Afghan"
        },
        {
            "code": "AL",
            "title": "Albanian"
        },
        {
            "code": "DZ",
            "title": "Algerian"
        },
        {
            "code": "US",
            "title": "American"
        },
        {
            "code": "UM",
            "title": "American"
        },
        {
            "code": "AS",
            "title": "American Samoan"
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

Endpoint: ``https://www.atlmoneytransfer.com/api/resources/check-gh-mw-instant-pay-eligibility``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------------------+
| Param                 | Mandatory        | Description                                                           |
+=======================+==================+=======================================================================+
| operator              | Yes              | Mobile operator code.                                                 |
+-----------------------+------------------+-----------------------------------------------------------------------+
| mobile_number         | Yes              | Mobile number to check.                                               |
+-----------------------+------------------+-----------------------------------------------------------------------+


**Request**

.. code-block:: console

  GET /api/resources/check-gh-mw-instant-pay-eligibility?operator=20e22bc1-50f5-11e7-9651-0ac5f86965eb&amp;mobile_number=24740XXXX HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "recipient_name": "FIRST LAST",
      "eligible_for_instant_pay": 1
  }


Validate account number for Instant Pay in Ghana
------------------------------------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/resources/check-gh-ac-instant-pay-eligibility``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------------------+
| Param                 | Mandatory        | Description                                                           |
+=======================+==================+=======================================================================+
| bank                  | Yes              | Bank code.                                                            |
+-----------------------+------------------+-----------------------------------------------------------------------+
| account_number        | Yes              | Account number to check.                                              |
+-----------------------+------------------+-----------------------------------------------------------------------+


**Request**

.. code-block:: console

  GET /api/resources/check-gh-ac-instant-pay-eligibility?bank=15184286-3ecc-46ab-872d-740f32e11d9c&amp;account_number=1126054XXXXXX HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "recipient_name": "FIRST LAST",
    "eligible_for_instant_pay": 1
  }
