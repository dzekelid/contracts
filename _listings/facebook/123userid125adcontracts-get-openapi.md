---
swagger: "2.0"
x-collection-name: Facebook
x-complete: 0
info:
  title: Facebook Get User Adcontracts
  description: User Adcontracts
  termsOfService: https://www.facebook.com/policies/
  version: 1.0.0
host: graph.facebook.com
basePath: /v3.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /&#123;user-id&#125;/adcontracts:
    get:
      summary: Get User Adcontracts
      description: User Adcontracts
      operationId: getUserAdcontracts
      x-api-path-slug: 123userid125adcontracts-get
      parameters:
      - in: query
        name: "200"
        description: Permissions error
        type: string
      - in: query
        name: "278"
        description: Reading advertisements requires an access token with the extended
          permission ads_read
        type: string
      responses:
        200:
          description: OK
      tags:
      - User
      - Adcontracts
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---