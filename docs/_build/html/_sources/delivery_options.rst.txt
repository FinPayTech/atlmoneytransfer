Delivery Options
================

To retrieve delivery options such as Mobile Operators, Utility Billers

Endpoint: ``https://www.atlmoneytransfer.com/api/delivery-options``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------------------+
| Param                 | Mandatory        | Description                                                           |
+=======================+==================+=======================================================================+
| country               | Yes              | Country code for which list of delivery options should be retrieved.  |
+-----------------------+------------------+-----------------------------------------------------------------------+
| payoutMethod          | Yes              | Payout method for which list of delivery options should be retrieved. |
+-----------------------+------------------+-----------------------------------------------------------------------+

**Request**

.. code-block:: console

  GET /api/delivery-options?country=GH&amp;payoutMethod=MW HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "delivery_options": [
        {
            "code": "03b2584b-7d04-4c5d-a0ba-3d2576c601f2",
            "title": "Airtel",
            "customer_identifier_label": "Mobile Number"
        },
        {
            "code": "20e22bc1-50f5-11e7-9651-0ac5f86965eb",
            "title": "MTN Mobile Money",
            "customer_identifier_label": "Mobile Number"
        },
        {
            "code": "66f176e2-a41f-400d-8246-976949912d3f",
            "title": "Tigo",
            "customer_identifier_label": "Mobile Number"
        },
        {
            "code": "f473e504-17bb-4198-9d42-fa0641c75c37",
            "title": "Vodafone",
            "customer_identifier_label": "Mobile Number"
        }
    ]
  }


**Response Description**

+---------------------------------------------------+------------------------------------------------------------------+
| Field                                             | Description                                                      |
+===================================================+==================================================================+
| delivery_options.{n}.code                         | Unique Identifier for delivery option.                           |
+---------------------------------------------------+------------------------------------------------------------------+
| delivery_options.{n}.title                        | Title of the delivery option.                                    |
+---------------------------------------------------+------------------------------------------------------------------+
| delivery_options.{n}.customer_identifier_label    | Label for customer identifier field.                             |
+---------------------------------------------------+------------------------------------------------------------------+
