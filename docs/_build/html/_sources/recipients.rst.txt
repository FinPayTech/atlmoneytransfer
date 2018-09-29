Recipient Object
================

The recipient object varies for each corridor and payout method.

Austria
-------

**Account Transfer to Austria**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.

Belgium
-------

**Account Transfer to Belgium**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Benin
-----

**Account Transfer to Benin**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Benin**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Burkina Faso
------------

**Account Transfer to Burkina Faso**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to Burkina Faso**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Cameroon
--------

**Account Transfer to Cameroon**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank_code                    | Yes         |  Bank's code.                                                     |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Cameroon**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Canada
------

**Account Transfer to Canada**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| institution_number           | Yes         |  Institution number of account.                                   |
+------------------------------+-------------+-------------------------------------------------------------------+
| transit_number               | Yes         |  Transit number of account.                                       |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of account.                                       |
+------------------------------+-------------+-------------------------------------------------------------------+
| swift_code                   | Yes         |  SWIFT of account.                                                |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_type                 | Yes         |  Either SAVINGS or CHECKING                                       |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Central African Republic
------------------------

**Account Transfer to Central African Republic**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank_code                    | Yes         |  Bank's code.                                                     |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Chad
----

**Account Transfer to Chad**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank_code                    | Yes         |  Bank's code.                                                     |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to Chad**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Congo
-----

**Account Transfer to Congo**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank_code                    | Yes         |  Bank's code.                                                     |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Côte d'Ivoire
-------------

**Account Transfer to Côte d'Ivoire**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to Côte d'Ivoire**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+



**Mobile Wallet to Côte d'Ivoire**

.. CAUTION::

  **Mobile Wallet to Côte d'Ivoire** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_operator              | Yes         |  Operate of mobile number. See Delivery Options section.          |
+------------------------------+-------------+-------------------------------------------------------------------+



Cyprus
------

**Account Transfer to Cyprus**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



Democratic Republic of the Congo
--------------------------------

**Cash Pickup to Democratic Republic of the Congo**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+



Denmark
-------

**Account Transfer to Denmark**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| registration_number          | Yes         |  Registration Number.                                             |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Denmark**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+



Equatorial Guinea
-----------------

**Account Transfer to Equatorial Guinea**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank_code                    | Yes         |  Bank's code.                                                     |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Estonia
-------

**Account Transfer to Estonia**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Finland
-------

**Account Transfer to Finland**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.




France
------

**Account Transfer to France**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to France**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Gabon
-----

**Account Transfer in Gabon**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank_code                    | Yes         |  Bank's code.                                                     |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to Gabon**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Gambia
------

**Cash Pickup to Gambia**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Germany
-------

**Account Transfer to Germany**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Ghana
-----

**Account Transfer in Ghana**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section.                                    |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| sort_code                    | No          |  Sort code of recipient's bank account.                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Ghana**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


**Mobile Wallet in Ghana**

.. CAUTION::

  **Mobile Wallet to Ghana** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_operator              | Yes         |  Operate of mobile number. See Delivery Options section.          |
+------------------------------+-------------+-------------------------------------------------------------------+


Greece
------

**Account Transfer to Greece**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.




Guinea
------

**Cash Pickup to Guinea**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Guinea-Bissau
-------------

**Account Transfer to Guinea-Bissau**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to Guinea-Bissau**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+



Ireland
-------

**Account Transfer to Ireland**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Italy
-----

**Account Transfer to Italy**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Latvia
------

**Account Transfer in Latvia**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Lithuania
---------

**Account Transfer in Lithuania**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



Luxembourg
----------

**Account Transfer in Luxembourg**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



Mali
----

**Account Transfer to Mali**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Mali**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Malta
-----

**Account Transfer in Malta**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



Netherlands
-----------

**Account Transfer in Netherlands**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



Niger
-----

**Account Transfer to Niger**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Niger**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+



Nigeria
-------

**Account Transfer to Nigeria**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section.                                    |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Portugal
--------

**Account Transfer to Portugal**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Senegal
-------

**Account Transfer to Senegal**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Senegal**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+



Sierra Leone
------------

**Account Transfer**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section.                                    |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to Sierra Leone**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


Slovakia
--------

**Account Transfer to Slovakia**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



Slovenia
--------

**Account Transfer to Slovenia**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


Spain
-----

**Account Transfer to Spain**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Complete bank name with no abbreviation.                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| iban                         | Yes         |  IBAN of the bank account.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



Togo
----

**Account Transfer to Togo**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section for codes.                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| branch_code                  | Yes         |  Account's branch code.                                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| rib_key                      | Yes         |  RIB Key                                                          |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | No          |  Mobile number of recipient, if available                         |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.


**Cash Pickup to Togo**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+



United Kingdom
--------------

**Account Transfer to United Kingdom**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section.                                    |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| sort_code                    | Yes         |  Sort code of recipient's bank account.                           |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient if available.                     |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.



**Cash Pickup to United Kingdom**

.. CAUTION::

  **Cash Pickup** service is only limited to individual recipients.

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Yes         |  First name of the recipient as it appears of recipient's ID.     |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Yes         |  Last name of the recipient as it appears of recipient's ID.      |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| mobile_number                | Yes         |  Mobile number of the recipient.                                  |
+------------------------------+-------------+-------------------------------------------------------------------+
| email                        | No          |  Email address of recipient, if available.                        |
+------------------------------+-------------+-------------------------------------------------------------------+


United States
-------------

**Account Transfer to United States**

+------------------------------+-------------+-------------------------------------------------------------------+
| Parameter                    | Mandatory   |  Description                                                      |
+==============================+=============+===================================================================+
| first_name                   | Conditional |  First name of the recipient as it appears of their bank account. |
+------------------------------+-------------+-------------------------------------------------------------------+
| last_name                    | Conditional |  Last name of the recipient as it appears of their bank account.  |
+------------------------------+-------------+-------------------------------------------------------------------+
| business_name                | Conditional |  | If recipient is company, name of the business as it appears    |
|                              |             |  | on their bank account.                                         |
+------------------------------+-------------+-------------------------------------------------------------------+
| bank                         | Yes         |  Bank code. See Banks section.                                    |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_number               | Yes         |  Account number of the recipient.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| routing_code                 | Yes         |  Routing code of recipient's bank account.                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| account_type                 | Yes         |  Any of SAVING OR CHECKING                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| address                      | Yes         |  Address of the recipient.                                        |
+------------------------------+-------------+-------------------------------------------------------------------+
| city                         | Yes         |  City where recipient is located.                                 |
+------------------------------+-------------+-------------------------------------------------------------------+
| region                       | No          |  Province/County/State/Region where recipient is located.         |
+------------------------------+-------------+-------------------------------------------------------------------+
| postcode                     | No          |  Postal code of area where recipient is located.                  |
+------------------------------+-------------+-------------------------------------------------------------------+

.. NOTE::

  | **first_name** and **last_name** are required for **individual** recipients.
  | **business_name** is required when recipient is a **company** or an **organization**.
