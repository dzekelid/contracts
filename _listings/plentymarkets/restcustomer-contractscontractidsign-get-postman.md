{
  "info": {
    "name": "Plentymarkets Returns signing of a contract",
    "_postman_id": "1bad35e4-1e63-4d39-882a-413d3cff0a8c",
    "description": "Returns signing of a contract.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "e5e409d3-3482-4f8e-8c4a-946a119d5a74",
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
              "id": "84eb7aab-c950-46f7-8dcf-9a54bb2c7f94"
            }
          ]
        }
      ]
    },
    {
      "name": "Creates",
      "item": [
        {
          "id": "ce7768a3-14e5-40b8-b1cf-631f6b5fd8da",
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
              "id": "6646be26-d9d9-492c-b562-2be076bdb05d"
            }
          ]
        }
      ]
    },
    {
      "name": "Returns",
      "item": [
        {
          "id": "42b8d079-ccaf-4195-9852-93fee8690d97",
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
              "id": "ec2a6ab7-bdd4-40f4-a32d-dd71c2d7561a"
            }
          ]
        },
        {
          "id": "dcda309d-01ec-49b2-82f1-0374210ca44c",
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
              "id": "451306bf-2bd3-4c81-aac4-25e1f0304d7d"
            }
          ]
        }
      ]
    },
    {
      "name": "Starts",
      "item": [
        {
          "id": "cde93c69-9c9a-475a-bd41-31e26c4ca06b",
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
              "id": "7ee632e9-cca1-4691-901e-a52e5e286000"
            }
          ]
        }
      ]
    }
  ]
}