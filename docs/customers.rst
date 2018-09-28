.. raw:: html

    <style> .red {color:red} .green{color:green}</style>


.. role:: red
.. role:: green

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


Create a Customer
-----------------

Endpoint: ``https://www.atlmoneytransfer.com/api/customers``

Method: ``POST``

+---------------------+------------+-------------------------------------------------------------------------+
| Parameter           | Mandatory  | Description                                                             |
+=====================+============+=========================================================================+
| first_name          | Yes        | First name of the customer as it appears on their Proof of Identity.    |
+---------------------+------------+-------------------------------------------------------------------------+
| middle_name         | No         | Middle name of the customer as it appears on their Proof of Identity.   |
+---------------------+------------+-------------------------------------------------------------------------+
| last_name           | Yes        | Last name of the customer as it appears on their Proof of Identity.     |
+---------------------+------------+-------------------------------------------------------------------------+
| date_of_birth       | Yes        | Date of birth of the customer as it appears on their Proof of Identity. |
+---------------------+------------+-------------------------------------------------------------------------+
| birth_city          | No         | Birth city of the customer.                                             |
+---------------------+------------+-------------------------------------------------------------------------+
| birth_country       | No         | Birth country of the customer.                                          |
+---------------------+------------+-------------------------------------------------------------------------+
| nationality         | Yes        | Current nationality of the customer.                                    |
+---------------------+------------+-------------------------------------------------------------------------+
| birth_nationality   | No         | Nationality of the customer at the time of birth.                       |
+---------------------+------------+-------------------------------------------------------------------------+
| address             | Yes        | Address of the customer.                                                |
+---------------------+------------+-------------------------------------------------------------------------+
| city                | Yes        | City where the customer is located.                                     |
+---------------------+------------+-------------------------------------------------------------------------+
| region              | No         | State/Province/Region where the customer is located.                    |
+---------------------+------------+-------------------------------------------------------------------------+
| postcode            | No         | Postcode of the area where the customer is located.                     |
+---------------------+------------+-------------------------------------------------------------------------+
| country             | Yes        | Country where the customer is located.                                  |
+---------------------+------------+-------------------------------------------------------------------------+
| phone_number        | No         | Phone number of the customer.                                           |
+---------------------+------------+-------------------------------------------------------------------------+
| mobile_number       | Yes        | Mobile number of the customer.                                          |
+---------------------+------------+-------------------------------------------------------------------------+
| email_address       | No         | Email address of the customer.                                          |
+---------------------+------------+-------------------------------------------------------------------------+

.. HINT::
   Since a resource is being created, HTTP response code ``201`` will be returned if the customer is successfully created.

**Request**

.. code-block:: console

  POST /api/customers HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx
  Content-Type: application/x-www-form-urlencoded

  first_name=Dhruv
  &middle_name=
  &last_name=Patel
  &date_of_birth=1989-11-04
  &birth_city=London
  &birth_country=GB
  &nationality=GB
  &birth_nationality=GB
  &address=ATL+House%2C+128+Peckham+Hill+Street
  &city=London
  &region=England
  &postcode=SE15+5JT
  &country=GB
  &phone_number=1234567890
  &mobile_number=9876543210
  &email_address=support%40atlmoneytransfer.com

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "customer": {
        "id": 9963210701,
        "first_name": "Dhruv",
        "middle_name": "",
        "last_name": "Patel",
        "date_of_birth": "1989-11-04",
        "birth_city": "London",
        "birth_country": "GB",
        "nationality": "GB",
        "birth_nationality": "GB",
        "address": "ATL House, 128 Peckham Hill Street",
        "city": "London",
        "region": "England",
        "postcode": "SE15 5JT",
        "country": "GB",
        "mobile_number": "9876543210",
        "phone_number": "1234567890",
        "email_address": "support@atlmoneytransfer.com",
        "blocked": 0,
        "temporary_blocked": 0,
        "created_on": "2018-09-28T08:40:11+00:00",
        "updated_on": "2018-09-28T08:40:11+00:00"
    }
  }

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
              "id": 9963210701,
              "first_name": "Dhruv",
              "middle_name": "",
              "last_name": "Patel",
              "date_of_birth": "1989-11-04",
              "birth_city": "London",
              "birth_country": "GB",
              "nationality": "GB",
              "birth_nationality": "GB",
              "address": "ATL House, 128 Peckham Hill Street",
              "city": "London",
              "region": "England",
              "postcode": "SE15 5JT",
              "country": "GB",
              "mobile_number": "9876543210",
              "phone_number": "1234567890",
              "email_address": "support@atlmoneytransfer.com",
              "blocked": 0,
              "temporary_blocked": 0,
              "created_on": "2018-09-28T08:40:11+00:00",
              "updated_on": "2018-09-28T08:40:11+00:00"
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
          "id": 9963210701,
          "first_name": "Dhruv",
          "middle_name": "",
          "last_name": "Patel",
          "date_of_birth": "1989-11-04",
          "birth_city": "London",
          "birth_country": "GB",
          "nationality": "GB",
          "birth_nationality": "GB",
          "address": "ATL House, 128 Peckham Hill Street",
          "city": "London",
          "region": "England",
          "postcode": "SE15 5JT",
          "country": "GB",
          "mobile_number": "9876543210",
          "phone_number": "1234567890",
          "email_address": "support@atlmoneytransfer.com",
          "blocked": 0,
          "temporary_blocked": 0,
          "created_on": "2018-09-28T08:40:11+00:00",
          "updated_on": "2018-09-28T08:40:11+00:00"
      }
  }

Update Customer Object
----------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/customers/:id``

Method: ``POST``

**Request**

.. code-block:: console

  POST /api/customers/9963210701 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx
  Content-Type: application/x-www-form-urlencoded

  last_name=Tester
  &date_of_birth=1990-12-04
  &postcode=SE15+5JT

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "customer": {
          "id": 9963210701,
          "first_name": "Dhruv",
          "middle_name": "",
          "last_name": "Tester",
          "date_of_birth": "1990-12-04",
          "birth_city": "London",
          "birth_country": "GB",
          "nationality": "GB",
          "birth_nationality": "GB",
          "address": "ATL House, 128 Peckham Hill Street",
          "city": "London",
          "region": "England",
          "postcode": "SE15 5JT",
          "country": "GB",
          "mobile_number": "9876543210",
          "phone_number": "1234567890",
          "email_address": "support@atlmoneytransfer.com",
          "blocked": 0,
          "temporary_blocked": 0,
          "created_on": "2018-09-28T08:40:11+00:00",
          "updated_on": "2018-09-28T09:40:35+00:00"
      }
  }

Customer KYC Document Object
----------------------------

+-------------+-------------------------------------------------------------------------+
| Parameter   | Description                                                             |
+=============+=========================================================================+
| type        | Document type of the uploaded KYC. Any of POI, POA, SOF                 |
+-------------+-------------------------------------------------------------------------+
| document    | Document of the uploaded KYC. Eg. PAS or DRV etc.                       |
+-------------+-------------------------------------------------------------------------+
| id_number   | Document ID Number of uploaded KYC.                                     |
+-------------+-------------------------------------------------------------------------+
| valid_from  | Document valid from date of the uploaded KYC.                           |
+-------------+-------------------------------------------------------------------------+
| expiry      | Document expiry date of the uploaded KYC.                               |
+-------------+-------------------------------------------------------------------------+
| verified    | 1, if document is verfied by ATL Money Transfer, else 0                 |
+-------------+-------------------------------------------------------------------------+
| uploaded_on | Date when the document was uploaded to ATL Money Transfer.              |
+-------------+-------------------------------------------------------------------------+

Get Customer KYC Documents
--------------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/kyc-documents/:id``

Method: ``GET``

**Request**

.. code-block:: console

  GET /api/kyc-documents/2618602080 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "documents": [
          {
              "type": "POI",
              "document": "PAS",
              "id_number": "123456",
              "valid_from": "2017-01-01T00:00:00",
              "expiry": "2037-12-31T00:00:00",
              "verified": 1,
              "uploaded_on": "2018-09-27T13:43:34+00:00"
          },
          {
              "type": "POA",
              "document": "BAS",
              "id_number": "142536",
              "valid_from": null,
              "expiry": null,
              "verified": 0,
              "uploaded_on": "2018-09-27T13:43:11+00:00"
          }
      ]
  }


Upload KYC for Customer
-----------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/kyc-upload/:id``

Method: ``POST``

+-------------+-----------+-------------------------------------------------------------+
| Parameter   | Mandatory | Description                                                 |
+=============+===========+=============================================================+
| type        | Yes       | Document type of the uploaded KYC. Any of POI, POA, SOF     |
+-------------+-----------+-------------------------------------------------------------+
| document    | Yes       | Document of the uploaded KYC. Eg. PAS or DRV etc.           |
+-------------+-----------+-------------------------------------------------------------+
| id_number   | Yes       | Document ID Number of uploaded KYC.                         |
+-------------+-----------+-------------------------------------------------------------+
| valid_from  | No        | Document valid from date of the uploaded KYC.               |
+-------------+-----------+-------------------------------------------------------------+
| expiry      | No        | Document expiry date of the uploaded KYC.                   |
+-------------+-----------+-------------------------------------------------------------+
| file        | Yes       | File to be uploaded. Only images and pdf are accepted.      |
+-------------+-----------+-------------------------------------------------------------+

.. HINT::
   Since a resource is being created, HTTP response code ``201`` will be returned if the kyc is successfully uploaded.

**Request**

.. code-block:: console

  POST /api/upload-kyc/9963210701 HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx
  Content-Type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW

  ------WebKitFormBoundary7MA4YWxkTrZu0gW
  Content-Disposition: form-data; name="type"

  POI
  ------WebKitFormBoundary7MA4YWxkTrZu0gW
  Content-Disposition: form-data; name="document"

  PAS
  ------WebKitFormBoundary7MA4YWxkTrZu0gW
  Content-Disposition: form-data; name="id_number"

  P123456
  ------WebKitFormBoundary7MA4YWxkTrZu0gW
  Content-Disposition: form-data; name="valid_from"

  2018-09-01
  ------WebKitFormBoundary7MA4YWxkTrZu0gW
  Content-Disposition: form-data; name="expiry"

  2028-08-31
  ------WebKitFormBoundary7MA4YWxkTrZu0gW
  Content-Disposition: form-data; name="file"; filename="Passport.jpg"
  Content-Type: image/jpeg


  ------WebKitFormBoundary7MA4YWxkTrZu0gW--

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "document": {
        "type": "POI",
        "document": "PAS",
        "id_number": "P123456",
        "valid_from": "2018-09-01",
        "expiry": "2028-08-31",
        "verified": 0,
        "uploaded_on": "2018-09-28T12:24:34+00:00"
    }
  }
