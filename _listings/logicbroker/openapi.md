swagger: "2.0"
x-collection-name: Logicbroker
x-complete: 1
info:
  title: CommerceAPI
  version: 1.0.0
host: stage.commerceapi.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1/Webhooks:
    post:
      summary: Create a new webhook
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Webhook_CreateWebhook
      x-api-path-slug: apiv1webhooks-post
      parameters:
      - in: body
        name: Webhook
        description: The new webhook
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Webhook
  /api/v1/Shipments/ContainerCode:
    get:
      summary: Gets a new SSCC18 container code.
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Shipment_GetContainerCode
      x-api-path-slug: apiv1shipmentscontainercode-get
      parameters:
      - in: query
        name: containerType
        description: Container type, valid types are box and pallet
      responses:
        200:
          description: OK
      tags:
      - S
      - New
      - SSCC18
      - Container
      - Code
  /api/v1/Shipments:
    post:
      summary: Create a new shipment
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Shipment_CreateShipment
      x-api-path-slug: apiv1shipments-post
      parameters:
      - in: body
        name: Shipment
        description: The shipment to save
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Shipment
  /api/v1/Invoices:
    post:
      summary: Create a new invoice
      description: Request rate limited to 10 requests per second with bursts up to
        100 requests.
      operationId: Invoice_CreateInvoice
      x-api-path-slug: apiv1invoices-post
      parameters:
      - in: body
        name: invoice
        description: The invoice to save
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Invoice