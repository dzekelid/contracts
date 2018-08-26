---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 1
info:
  title: plentymarkets REST-API
  description: the-plentymarkets-rest-api-expands-the-functionality-of-the-plentymarkets-cms-and-allows-access-to-resources-i-e--data-records-via-unique-uri-paths
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/customer_contracts:
    get:
      summary: List contracts
      description: List contracts.
      operationId: getRestCustomerContracts
      x-api-path-slug: restcustomer-contracts-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Contracts
    post:
      summary: Creates a new contract
      description: Creates a new contract.
      operationId: postRestCustomerContracts
      x-api-path-slug: restcustomer-contracts-post
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Contract
  /rest/customer_contracts/{contractId}:
    get:
      summary: Returns a single contract
      description: Returns a single contract.
      operationId: getRestCustomerContractsContract
      x-api-path-slug: restcustomer-contractscontractid-get
      parameters:
      - in: path
        name: contractId
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Single
      - Contract
  /rest/customer_contracts/{contractId}/document:
    get:
      summary: Starts download of contract document
      description: Starts download of contract document.
      operationId: getRestCustomerContractsContractDocument
      x-api-path-slug: restcustomer-contractscontractiddocument-get
      parameters:
      - in: path
        name: contractId
      responses:
        200:
          description: OK
      tags:
      - Starts
      - Download
      - Of
      - Contract
      - Document
  /rest/customer_contracts/{contractId}/sign:
    get:
      summary: Returns signing of a contract
      description: Returns signing of a contract.
      operationId: getRestCustomerContractsContractSign
      x-api-path-slug: restcustomer-contractscontractidsign-get
      parameters:
      - in: path
        name: contractId
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Signing
      - Of
      - Contract
    post:
      summary: Sign a contract
      description: Sign a contract.
      operationId: postRestCustomerContractsContractSign
      x-api-path-slug: restcustomer-contractscontractidsign-post
      parameters:
      - in: path
        name: contractId
      responses:
        200:
          description: OK
      tags:
      - Sign
      - Contract
  /rest/customer_contracts/{contractId}/sign/document:
    get:
      summary: Starts download of signed contract document
      description: Starts download of signed contract document.
      operationId: getRestCustomerContractsContractSignDocument
      x-api-path-slug: restcustomer-contractscontractidsigndocument-get
      parameters:
      - in: path
        name: contractId
      responses:
        200:
          description: OK
      tags:
      - Starts
      - Download
      - Of
      - Signed
      - Contract
      - Document
---