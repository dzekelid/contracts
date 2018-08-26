{
  "info": {
    "name": "Plentymarkets Sign a contract",
    "_postman_id": "05bc3078-3fd1-4d9a-9810-d4a76cc5fef4",
    "description": "Sign a contract.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "f4af570e-fd91-402d-b2e0-fbdc1a432110",
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
              "id": "6e5f957f-b715-4c49-83d3-c03d30daad38"
            }
          ]
        }
      ]
    },
    {
      "name": "Creates",
      "item": [
        {
          "id": "44e12f9d-2d65-4438-812a-368233553189",
          "name": "postRestCustomerContracts",
          "request": {
            "url": "http://example.com/rest/customer_contracts",
            "method": "POST",
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
            "description": "Creates a new contract."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d64695f4-31ff-4f7b-8cca-c1841a03ca0e"
            }
          ]
        }
      ]
    },
    {
      "name": "Returns",
      "item": [
        {
          "id": "02a51c6b-116a-4fb0-820d-8dc5034414bf",
          "name": "getRestCustomerContractsContract",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/customer_contracts/:contractId"
              ],
              "variable": [
                {
                  "id": "contractId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "Returns a single contract."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d45acd39-2a32-49b5-87b2-b77b9c2b316d"
            }
          ]
        },
        {
          "id": "b550ee60-112f-4e7a-bd48-d72dd9745b28",
          "name": "getRestCustomerContractsContractSign",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/customer_contracts/:contractId/sign"
              ],
              "variable": [
                {
                  "id": "contractId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "Returns signing of a contract."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4f283b36-0ba6-4b6a-b9c7-0581cc1a7401"
            }
          ]
        }
      ]
    },
    {
      "name": "Starts",
      "item": [
        {
          "id": "8439f1fd-8644-4907-9750-74ad236c716e",
          "name": "getRestCustomerContractsContractDocument",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/customer_contracts/:contractId/document"
              ],
              "variable": [
                {
                  "id": "contractId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
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
            "description": "Starts download of contract document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "683622fb-e199-46f8-9ad5-eb831bdccd7f"
            }
          ]
        }
      ]
    },
    {
      "name": "Sign",
      "item": [
        {
          "id": "fd339b08-81c5-4ccd-af18-be67a7061aa9",
          "name": "postRestCustomerContractsContractSign",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/customer_contracts/:contractId/sign"
              ],
              "variable": [
                {
                  "id": "contractId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
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
            "description": "Sign a contract."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "65310fa0-5e0a-4647-8ea6-a09eafcc5342"
            }
          ]
        }
      ]
    }
  ]
}