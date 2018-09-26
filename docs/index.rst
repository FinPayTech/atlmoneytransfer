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
