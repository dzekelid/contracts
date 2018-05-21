---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite Futures
  description: provide-delayed-and-historical-commodity-quote-information-from-supported-exchanges-nymex
  version: 1.0.0
host: www.xignite.com
basePath: xFutures.json/XigniteFutures
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ListFrontMonthContracts:
    post:
      summary: List Front Month Contracts
      description: List all commodity future Front Month Contracts.
      operationId: postListfrontmonthcontracts
      x-api-path-slug: listfrontmonthcontracts-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - List
      - Front
      - Month
      - Contracts
---