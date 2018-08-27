{
  "info": {
    "name": "Plentymarkets Returns a single contract",
    "_postman_id": "7503e585-c7f2-4dba-913a-acf2e6fcccda",
    "description": "Returns a single contract.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Single",
      "item": [
        {
          "id": "0e7158ef-9393-48d0-833a-532e63f2f9b7",
          "name": "getRestAccountsContactsContactDocument",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/accounts/contacts/:contactId/document"
              ],
              "query": [
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contactId",
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
            "description": "Get a single storage object from contact documents."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "37d9fa83-786d-4601-800f-4b7de9618b74"
            }
          ]
        }
      ]
    },
    {
      "name": "Temporary",
      "item": [
        {
          "id": "f00feedd-5cce-4d44-a5be-a7e93ee3a87a",
          "name": "getRestAccountsContactsContactDocumentUrl",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/accounts/contacts/:contactId/document/url"
              ],
              "query": [
                {
                  "key": "key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contactId",
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
            "description": "Get a temporary url for a single document."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06998aeb-9769-40da-8523-d21c0993577b"
            }
          ]
        }
      ]
    },
    {
      "name": "List",
      "item": [
        {
          "id": "5aade07f-1221-46b6-a756-19849256ffab",
          "name": "getRestAccountsContactsContactDocuments",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/accounts/contacts/:contactId/documents"
              ],
              "query": [
                {
                  "key": "continuationToken",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "contactId",
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
            "description": "List documents for a single contact."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a5495f2a-3842-482e-8fc6-7f27585117ac"
            }
          ]
        }
      ]
    },
    {
      "name": "S",
      "item": [
        {
          "id": "29313b70-91f3-4df0-80b2-c8e5b1128115",
          "name": "getRestBoardsBoard",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/boards/:boardId"
              ],
              "query": [
                {
                  "key": "tasksPerPage",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "boardId",
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
            "description": "Gets a single board by its id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "162e3293-15e9-4934-acf5-a95873dc2651"
            }
          ]
        }
      ]
    },
    {
      "name": "Returns",
      "item": [
        {
          "id": "62c3caec-4545-446c-8b23-0ed5f5075a4d",
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
              "id": "19abc531-3f34-41d1-a863-155c55b3c2d1"
            }
          ]
        }
      ]
    }
  ]
}