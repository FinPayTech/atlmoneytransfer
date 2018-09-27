Customer Object
===============

Customer objects allow you to perform transactions easily. It is highly recommended that partner should store customer id returned from ATL Money Transfer and should use customer id for all future transactions from the same customer.

+--------------------------+-------------------------------------------------------------------------+
| Parameter                | Description                                                             |
+==========================+=========================================================================+
| id                       | Global unique identifier for customer.                                  |
+--------------------------+-------------------------------------------------------------------------+
| first_name               | First name of the customer as it appears on their Proof of Identity.    |
+--------------------------+-------------------------------------------------------------------------+
| middle_name              | Middle name of the customer as it appears on their Proof of Identity.   |
+--------------------------+-------------------------------------------------------------------------+
| last_name                | Last name of the customer as it appears on their Proof of Identity.     |
+--------------------------+-------------------------------------------------------------------------+
| date_of_birth            | Date of birth of the customer as it appears on their Proof of Identity. |
+--------------------------+-------------------------------------------------------------------------+
| birth_city               | Birth city of the customer.                                             |
+--------------------------+-------------------------------------------------------------------------+
| birth_country            | Birth country of the customer.                                          |
+--------------------------+-------------------------------------------------------------------------+
| nationality              | Current nationality of the customer.                                    |
+--------------------------+-------------------------------------------------------------------------+
| birth_nationality        | Nationality of the customer at the time of birth.                       |
+--------------------------+-------------------------------------------------------------------------+
| address                  | Address of the customer.                                                |
+--------------------------+-------------------------------------------------------------------------+
| city                     | City where the customer is located.                                     |
+--------------------------+-------------------------------------------------------------------------+
| region                   | State/Province/Region where the customer is located.                    |
+--------------------------+-------------------------------------------------------------------------+
| postcode                 | Postcode of the area where the customer is located.                     |
+--------------------------+-------------------------------------------------------------------------+
| country                  | Country where the customer is located.                                  |
+--------------------------+-------------------------------------------------------------------------+
| phone_number             | Phone number of the customer.                                           |
+--------------------------+-------------------------------------------------------------------------+
| mobile_number            | Mobile number of the customer.                                          |
+--------------------------+-------------------------------------------------------------------------+
| email_address            | Email address of the customer.                                          |
+--------------------------+-------------------------------------------------------------------------+
| blocked                  | | 1 if customer is blocked for sending, else 0. Contact support         |
|                          | | for more information.                                                 |
+--------------------------+-------------------------------------------------------------------------+
| temporary_blocked        | | 1 if customer is blocked for sending on temporary basis. This         |
|                          | | usually happens due to compliance issue or suspicious activity.       |
|                          | | Contact support for more information.                                 |
+--------------------------+-------------------------------------------------------------------------+
| created_on               | Customer creation date of the customer on ATL Money Transfer.           |
+--------------------------+-------------------------------------------------------------------------+
| updated_on               | Date when customer was last updated.                                    |
+--------------------------+-------------------------------------------------------------------------+
| documents.{n}.type       | Document type of the uploaded KYC. Any of POI, POA, SOF                 |
+--------------------------+-------------------------------------------------------------------------+
| documents.{n}.document   | Document of the uploaded KYC. Eg. PAS or DRV etc.                       |
+--------------------------+-------------------------------------------------------------------------+
| documents.{n}.id_number  | Document ID Number of uploaded KYC.                                     |
+--------------------------+-------------------------------------------------------------------------+
| documents.{n}.valid_from | Document valid from date of the uploaded KYC.                           |
+--------------------------+-------------------------------------------------------------------------+
| documents.{n}.valid_to   | Document valid through date of the uploaded KYC.                        |
+--------------------------+-------------------------------------------------------------------------+
| documents.{n}.verified   | 1, if document is verfied by ATL Money Transfer, else 0                 |
+--------------------------+-------------------------------------------------------------------------+

Create a Customer
-----------------

Get List of all Customers
-------------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/customers``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------+
| Param                 | Mandatory        | Description                                               |
+=======================+==================+===========================================================+
| page                  | No               | Page number of result set.                                |
+-----------------------+------------------+-----------------------------------------------------------+

**Request**

.. code-block:: console

  GET /api/customers HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "customers": [
          {
              "id": 2618602080,
              "first_name": "Dhruv",
              "middle_name": "",
              "last_name": "Tester",
              "date_of_birth": "2000-09-02",
              "birth_city": "London",
              "birth_country": "GB",
              "nationality": "GB",
              "birth_nationality": "GB",
              "address": "128 Peckham Hill Street",
              "city": "London",
              "region": "",
              "postcode": "SE15 5JT",
              "country": "GB",
              "mobile_number": "1234567890",
              "phone_number": "",
              "email_address": "",
              "blocked": 0,
              "temporary_blocked": 0,
              "created_on": "2018-09-12T07:57:57+00:00",
              "updated_on": "2018-09-27T13:44:18+00:00"
          }
      ],
      "current_customers": 1,
      "total_customers": 1,
      "page": 1,
      "total_pages": 1
  }

**Response Description**

+----------------------------------+-------------------------------------------------------------------+
| Parameter                        | Description                                                       |
+==================================+===================================================================+
| customers.{n}.id                 | Global unique identifier for customer.                            |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.first_name         | First name of the customer.                                       |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.middle_name        | Middle name of the customer.                                      |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.last_name          | Last name of the customer.                                        |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.date_of_birth      | Date of birth of the customer.                                    |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.birth_city         | Birth city of the customer.                                       |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.birth_country      | Birth country of the customer.                                    |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.nationality        | Current nationality of the customer.                              |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.birth_nationality  | Nationality of the customer at the time of birth.                 |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.address            | Address of the customer.                                          |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.city               | City where the customer is located.                               |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.region             | State/Province/Region where the customer is located.              |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.postcode           | Postcode of the area where the customer is located.               |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.country            | Country where the customer is located.                            |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.phone_number       | Phone number of the customer.                                     |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.mobile_number      | Mobile number of the customer.                                    |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.email_address      | Email address of the customer.                                    |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.blocked            | 1 if customer is blocked for sending, else 0                      |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.temporary_blocked  | 1 if customer is blocked for sending on temporary basis, else 0   |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.created_on         | Customer creation date of the customer on ATL Money Transfer.     |
+----------------------------------+-------------------------------------------------------------------+
| customers.{n}.updated_on         | Date when customer was last updated.                              |
+----------------------------------+-------------------------------------------------------------------+
| current_customers                | Number of customer results on current page.                       |
+----------------------------------+-------------------------------------------------------------------+
| total_customers                  | Total number of customers on ATL Money Transfer Platform.         |
+----------------------------------+-------------------------------------------------------------------+
| page                             | Current page number.                                              |
+----------------------------------+-------------------------------------------------------------------+
| total_pages                      | Total number of pages.                                            |
+----------------------------------+-------------------------------------------------------------------+

Get Single Customer
-------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/customers/:id``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/customers/2618602080 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "customer": {
          "id": 2618602080,
          "first_name": "Dhruv",
          "middle_name": "",
          "last_name": "Tester",
          "date_of_birth": "2000-09-02",
          "birth_city": "London",
          "birth_country": "GB",
          "nationality": "GB",
          "birth_nationality": "GB",
          "address": "128 Peckham Hill Street",
          "city": "London",
          "region": "",
          "postcode": "SE15 5JT",
          "country": "GB",
          "mobile_number": "1234567890",
          "phone_number": "",
          "email_address": "",
          "blocked": 0,
          "temporary_blocked": 0,
          "created_on": "2018-09-12T07:57:57+00:00",
          "updated_on": "2018-09-27T13:44:18+00:00"
      }
  }

Update Customer Object
----------------------

Get Customer KYC Documents
--------------------------

Upload KYC
----------

Get Recipients of Customer
--------------------------

Get Customer Transaction List
-----------------------------
