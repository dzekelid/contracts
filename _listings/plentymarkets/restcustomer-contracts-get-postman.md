{
  "info": {
    "name": "Plentymarkets List contracts",
    "_postman_id": "874076fc-58dc-41a9-ac23-ad8de6d4ae3e",
    "description": "List contracts.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "cb60a4be-f89c-4d80-b2b8-a3790368b0bf",
          "name": "getRestCustomerContracts",
          "request": {
            "url": "http://example.com/rest/customer_contracts",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "List contracts."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1de978a4-c70d-4f11-bbbe-e23581994717"
            }
          ]
        }
      ]
    }
  ]
}