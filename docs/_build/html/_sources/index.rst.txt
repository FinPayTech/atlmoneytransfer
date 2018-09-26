.. toctree::
   :maxdepth: 2
   :caption: Table of Contents:




Introduction
============

The ATL Money Transfer API referred here as ATLMT API is organized around REST. Our API has predictable, resource-oriented URLs, and uses HTTP response codes to indicate API errors. We use built-in HTTP features, like HTTP authentication and HTTP verbs, which are understood by off-the-shelf HTTP clients. We support cross-origin resource sharing, allowing you to interact securely with our API from a client-side web application (though you should never expose your secret API key in any public website's client-side code). JSON is returned by all API responses, including errors, although our API libraries convert responses to appropriate language-specific objects.

To make the API as explorable as possible, accounts have test mode and live mode API keys. There is no "switch" for changing between modes, just use the appropriate key to perform a live or test transaction. Requests made with test mode credentials never hit the banking networks and incur no cost.

Authentication
==============

Authentication to the API is performed via bearer auth (e.g., for a cross-origin request), use -H "Authorization: Bearer sandbox_5ba22ce43aa945ba22ce43ab3b"

All API requests must be made over HTTPS. Calls made over plain HTTP will fail. API requests without authentication will also fail.


Errors
======

ATLMT uses conventional HTTP response codes to indicate the success or failure of an API request. In general: Codes in the 2xx range indicate success. Codes in the 4xx range indicate an error that failed given the information provided (e.g., a required parameter was omitted, a charge failed, etc.). Codes in the 5xx range indicate an error with ATLMT's servers (these are rare).

Some 4xx errors that could be handled programmatically (e.g., an invalid account number) include an error code that briefly explains the error reported.

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
| 500              | Something went wrong on ATLMT’s end. (These are rare.)                    |
+------------------+---------------------------------------------------------------------------+

Error Types
-----------

+-----------------------+-----------------------------------------------------------------------------+
| Type                  | Description                                                                 |
+=======================+=============================================================================+
| api_connection_error  | Failure to connect to ATLMT's API.                                          |
+-----------------------+-----------------------------------------------------------------------------+
| api_error             | API errors cover any other type of problem (e.g., a temporary               |
|                       | problem with ATLMT’s or 3rd Party’s servers), and are extremely uncommon.   |
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
