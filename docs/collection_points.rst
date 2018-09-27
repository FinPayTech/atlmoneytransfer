Cash Collection Points
======================

Get list of all payout partners in country
------------------------------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/cash-collection-partners``

Method: ``GET``

+-----------------------+------------------+--------------------------------------------------------------+
| Param                 | Mandatory        | Description                                                  |
+=======================+==================+==============================================================+
| country               | Yes              | Country code for which list of partners should be retrieved. |
+-----------------------+------------------+--------------------------------------------------------------+

**Request**

.. code-block:: console

  GET /api/cash-collection-partners?country=CI HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "partners": [
          {
              "code": "ATLCI",
              "title": "ATL Money Transfer, CI",
              "information": "Partner can payout any ATL network transaction within the country."
          },
          {
              "code": "GTBCI",
              "title": "GT Bank, CI",
              "information": "Partner can payout any ATL network transaction within the country."
          },
          {
              "code": "SOFIN",
              "title": "SOFINTEC",
              "information": "Partner can payout any ATL network transaction within the country."
          },
          {
              "code": "SRFIN",
              "title": "SERFIN",
              "information": "Partner can payout any ATL network transaction within the country."
          },
          {
              "code": "WARI",
              "title": "Wari",
              "information": "Partner can only payout transactions which are explicitly sent to this partner."
          }
      ]
  }

Get list of all collection points for partner in country
--------------------------------------------------------

Endpoint: ``https://www.atlmoneytransfer.com/api/cash-points``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------------------+
| Param                 | Mandatory        | Description                                                           |
+=======================+==================+=======================================================================+
| country               | Yes              | Country code for which list of collection points should be retrieved. |
+-----------------------+------------------+-----------------------------------------------------------------------+
| partner               | Yes              | Partner code for which list of collection points should be retrieved. |
+-----------------------+------------------+-----------------------------------------------------------------------+

**Request**

.. code-block:: console

  GET /api/collection-points?country=CI&amp;partner=GTBCI HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
      "message": "success",
      "locations": [
          {
              "name": "GTBank - Adjame",
              "address": "Boulevard Nangui Abrogoua, Face à la mosquée",
              "city": "Abidjan",
              "region": "",
              "postcode": "",
              "emails": [],
              "contacts": [
                  "+225 20311500"
              ],
              "information": "",
              "business_hours": {
                  "monday": {
                      "opens": "09:00 AM",
                      "closes": "04:00 PM"
                  },
                  "tuesday": {
                      "opens": "09:00 AM",
                      "closes": "04:00 PM"
                  },
                  "wednesday": {
                      "opens": "09:00 AM",
                      "closes": "04:00 PM"
                  },
                  "thursday": {
                      "opens": "09:00 AM",
                      "closes": "04:00 PM"
                  },
                  "friday": {
                      "opens": "09:00 AM",
                      "closes": "04:00 PM"
                  },
                  "saturday": {
                      "opens": "10:00 AM",
                      "closes": "01:00 PM"
                  },
                  "sunday": {
                      "opens": "Closed",
                      "closes": "Closed"
                  }
              }
          }
      ]
  }
