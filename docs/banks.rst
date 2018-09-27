Banks
=====

Endpoint: ``https://www.atlmoneytransfer.com/api/banks``

Method: ``GET``

+-----------------------+------------------+-----------------------------------------------------------+
| Param                 | Mandatory        | Description                                               |
+=======================+==================+===========================================================+
| country               | Yes              | Country code for which list of banks should be retrieved. |
+-----------------------+------------------+-----------------------------------------------------------+

**Request**

.. code-block:: console

  GET /api/banks?country=GH HTTP/1.1
  Host: www.atlmoneytransfer.com
  Authorization: Bearer sandbox_5ba9df637e1cd5baxxxxxxxxxx

**Response**

.. code-block:: JSON

  {
    "message": "success",
    "banks": [
        {
            "code": "44f18ca3-c3b1-4c3a-bebb-ade97ef335c7",
            "title": "Access Bank (AB)"
        },
        {
            "code": "a3ebb603-e2d6-45d2-babe-37bfb89bd270",
            "title": "Agricultural Development Bank of Ghana (ADB)"
        },
        {
            "code": "c6bdda4b-d3be-4c46-b8fc-4fa0823396cd",
            "title": "CAL Bank (CAL)"
        },
        {
            "code": "82215df8-b4df-44da-923e-1ddd7896bec7",
            "title": "Capital Bank"
        },
        {
            "code": "2e40651c-061e-48f1-97ab-84952bbbf9ef",
            "title": "Ecobank Ghana (Eco)"
        },
        {
            "code": "63cb76e7-c989-42b5-9122-c3b10f93d36a",
            "title": "Energy Bank (EB)"
        },
        {
            "code": "95e45c4a-87ae-4aae-be33-762362797db6",
            "title": "Fidelity Bank"
        },
        {
            "code": "b5c66e26-95de-4c9d-9bae-4361b632583e",
            "title": "Ghana Commercial Bank (GCB)"
        },
        {
            "code": "877dd227-3419-43b0-8562-8497b9868410",
            "title": "GN Bank Ghana (GN)"
        },
        {
            "code": "aed84bb7-9e12-47b9-b7d5-75c1ff646fad",
            "title": "Guaranty Trust Bank (GTB)"
        },
        {
            "code": "f670239d-c4f1-4c82-a87f-3b80e9d35d0d",
            "title": "HFC Bank (HFC)"
        },
        {
            "code": "15184286-3ecc-46ab-872d-740f32e11d9c",
            "title": "National Investment Bank (NIB)"
        },
        {
            "code": "f9c9d22b-afa2-4e92-9e4e-55f8df50f1a5",
            "title": "Prudential Bank (PB)"
        },
        {
            "code": "e836bdf7-3f95-4c02-bdd9-9170b52d634f",
            "title": "Stanbic Bank (SB)"
        },
        {
            "code": "c73896d7-3042-4641-af69-e4021d3c44b8",
            "title": "Standard Chartered Ghana (SCG)"
        },
        {
            "code": "4d06644d-690e-4d00-8a02-c5051c9c3f56",
            "title": "The Royal Bank (TRB)"
        },
        {
            "code": "5a16d3da-7970-40d1-b209-f5b729d6df2f",
            "title": "United Bank for Africa (UBA)"
        },
        {
            "code": "e6de9773-ef3f-4a62-8edd-58cb7c9366e0",
            "title": "Universal Merchant Bank (UMB)"
        },
        {
            "code": "a54de746-2c38-46c6-bf72-140b970d885b",
            "title": "Zenith Bank (ZB)"
        }
    ]
  }
