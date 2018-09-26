Errors
======

ATLMT uses conventional HTTP response codes to indicate the success or failure of an API request. In general: Codes in the `2xx` range indicate success. Codes in the `4xx` range indicate an error that failed given the information provided (e.g., a required parameter was omitted, a transaction failed, etc.). Codes in the `5xx` range indicate an error with ATLMT's servers (these are rare).

Some `4xx` errors that could be handled programmatically (e.g., an invalid account number) include an error code that briefly explains the error reported.

HTTP status code summary
------------------------

+------------------+---------------------------------------------------------------------------+
| HTTP Status Code | Description                                                               |
+==================+===========================================================================+
| 200              | Everything worked as expected.                                            |
+------------------+---------------------------------------------------------------------------+
| 201              | A new resource was created.                                               |
+------------------+---------------------------------------------------------------------------+
| 400              | The request was unacceptable, often due to missing a required parameter.  |
+------------------+---------------------------------------------------------------------------+
| 401              | No valid API key provided.                                                |
+------------------+---------------------------------------------------------------------------+
| 402              | The parameters were valid but the request failed.                         |
+------------------+---------------------------------------------------------------------------+
| 403              | You are not allowed to access this resource.                              |
+------------------+---------------------------------------------------------------------------+
| 404              | The requested resource doesn't exist.                                     |
+------------------+---------------------------------------------------------------------------+
| 405              | The request method is not allowed for invoked endpoint.                   |
+------------------+---------------------------------------------------------------------------+
| 500              | Something went wrong on ATLMT's end. (These are rare.)                    |
+------------------+---------------------------------------------------------------------------+

Error Types
-----------

+-----------------------+-----------------------------------------------------------------------------+
| Type                  | Description                                                                 |
+=======================+=============================================================================+
| api_connection_error  | Failure to connect to ATLMT's API.                                          |
+-----------------------+-----------------------------------------------------------------------------+
| api_error             | | API errors cover any other type of problem (e.g., a temporary             |
|                       | | problem with ATLMT’s or 3rd Party’s servers), and are extremely uncommon. |
+-----------------------+-----------------------------------------------------------------------------+
| authentication_error  | Failure to properly authenticate yourself in the request.                   |
+-----------------------+-----------------------------------------------------------------------------+
| authorization_error   | Trying to access restricted resource.                                       |
+-----------------------+-----------------------------------------------------------------------------+
| invalid_request_error | Invalid request errors arise when your request has invalid parameters.      |
+-----------------------+-----------------------------------------------------------------------------+


Handling Errors
---------------

Our API raise exceptions for many reasons, such as a failed transfer, invalid parameters, authentication errors, and network unavailability. We recommend writing code that gracefully handles all possible API exceptions.

+-----------------------+-----------------------------------------------------------------------------------+
| Attribute             | Description                                                                       |
+=======================+===================================================================================+
| type                  | Failure to connect to ATLMT's API.                                                |
+-----------------------+-----------------------------------------------------------------------------------+
| code                  | | For some errors that could be handled programmatically.                         |
|                       | | A short string indicating the error code reported. See Error Codes section.     |
+-----------------------+-----------------------------------------------------------------------------------+
| message               | A human-readable message providing more details about the error.                  |
+-----------------------+-----------------------------------------------------------------------------------+
| param                 | | If the error is parameter-specific, the parameter related to the error.         |
|                       | | For example, you can use this to display a message near the correct form field. |
+-----------------------+-----------------------------------------------------------------------------------+


Error Codes
-----------

Some `4xx` errors that could be handled programmatically (e.g., request contains invalid parameter) include an error code—a short string with a brief explanation—as a value for code. Below is a list of possible error codes that can be returned.

+-----------------------------------+-----------------------------------------------------------------------------------+
| Code                              | Description                                                                       |
+===================================+===================================================================================+
| parameter_missing                 | One or more required parameters are missing.                                      |
+-----------------------------------+-----------------------------------------------------------------------------------+
| parameter_empty                   | One or more required fields contain empty value.                                  |
+-----------------------------------+-----------------------------------------------------------------------------------+
| parameter_invalid                 | One or more required values are invalid.                                          |
+-----------------------------------+-----------------------------------------------------------------------------------+
| amount_too_large                  | | The specified amount is greater than the maximum amount allowed.                |
|                                   | | Use a lower amount and try again.                                               |
+-----------------------------------+-----------------------------------------------------------------------------------+
| amount_too_small                  | | The specified amount is less than the minimum amount allowed.                   |
|                                   | | Use a higher amount and try again.                                              |
+-----------------------------------+-----------------------------------------------------------------------------------+
| transaction_already_cancelled     | Transaction is already in Cancelled state.                                        |
+-----------------------------------+-----------------------------------------------------------------------------------+
| transaction_already_paid          | Transaction is already in Paid state.                                             |
+-----------------------------------+-----------------------------------------------------------------------------------+
| transaction_cancel_not_allowed    | Transaction cancellation is not allowed.                                          |
+-----------------------------------+-----------------------------------------------------------------------------------+
| country_unsupported               | Provided country is not supported.                                                |
+-----------------------------------+-----------------------------------------------------------------------------------+
| currency_unsupported              | Provided currency is not supported.                                               |
+-----------------------------------+-----------------------------------------------------------------------------------+
| processing_error                  | An error occurred while processing the request.                                   |
+-----------------------------------+-----------------------------------------------------------------------------------+
| sandbox_transactions_only         | | Your account has not been activated for live transactions.                      |
|                                   | | Contact your account manager.                                                   |
+-----------------------------------+-----------------------------------------------------------------------------------+
| tls_version_unsupported           | | Your integration is using an older version of TLS that is unsupported.          |
|                                   | | You must be using TLS 1.2 or above.                                             |
+-----------------------------------+-----------------------------------------------------------------------------------+
