---
swagger: "2.0"
x-collection-name: AXA Assistance
x-complete: 0
info:
  title: AXA Assistance Create new individual travel quote for sales
  description: Create new individual travel quote for sales
  version: 1.0.0
host: sandbox.api.axa-assistance.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /service/vexp/roadside/assignments:
    post:
      summary: Creates new assignment.
      description: Creates new assignment.
      operationId: postServiceVexpRoadsideAssignments
      x-api-path-slug: servicevexproadsideassignments-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Insurance
      - CreateAssistance
      - new
      - assignment.
  /sales/v1/individual/travel/policies:
    post:
      summary: Create new individual travel policy for sales
      description: Create new individual travel policy for sales
      operationId: postSalesV1IndividualTravelPolicies
      x-api-path-slug: salesv1individualtravelpolicies-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Insurance
      - new
      - individual
      - travel
      - policysales
  /sales/v1/individual/travel/quotes:
    post:
      summary: Create new individual travel quote for sales
      description: Create new individual travel quote for sales
      operationId: postSalesV1IndividualTravelQuotes
      x-api-path-slug: salesv1individualtravelquotes-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Insurance
      - new
      - individual
      - travel
      - quotesales
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