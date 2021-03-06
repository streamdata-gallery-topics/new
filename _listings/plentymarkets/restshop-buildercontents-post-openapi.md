---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Create a new content.
  description: Create a new content..
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
  /rest/boards:
    post:
      summary: Creates a new board.
      description: Creates a new board..
      operationId: postRestBoards
      x-api-path-slug: restboards-post
      parameters:
      - in: body
        name: /rest/boards
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Board
  /rest/boards/{boardId}/columns:
    post:
      summary: Creates a new column and assigns it to a given board
      description: Creates a new column and assigns it to a given board.
      operationId: postRestBoardsBoardColumns
      x-api-path-slug: restboardsboardidcolumns-post
      parameters:
      - in: body
        name: /rest/boards/{boardId}/columns
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: boardId
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Column
      - Assigns
      - It
      - To
      - Given
      - Board
  /rest/boards/{boardId}/columns/{columnId}/tasks:
    post:
      summary: Creates a new tasks on a specified column.
      description: Creates a new tasks on a specified column..
      operationId: postRestBoardsBoardColumnsColumnTasks
      x-api-path-slug: restboardsboardidcolumnscolumnidtasks-post
      parameters:
      - in: body
        name: /rest/boards/{boardId}/columns/{columnId}/tasks
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: boardId
      - in: path
        name: columnId
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Tasks
      - "On"
      - Specified
      - Column
  /rest/boards/{boardId}/columns/{columnId}/tasks/{taskId}/references:
    post:
      summary: Creates a new reference from a given task to a contact or a ticket.
      description: Creates a new reference from a given task to a contact or a ticket..
      operationId: postRestBoardsBoardColumnsColumnTasksTaskReferences
      x-api-path-slug: restboardsboardidcolumnscolumnidtaskstaskidreferences-post
      parameters:
      - in: path
        name: boardId
      - in: path
        name: columnId
      - in: query
        name: referenceValue
        description: Reference type followed by foreign ID of the referenced object
      - in: path
        name: taskId
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Reference
      - From
      - Given
      - Task
      - To
      - Contact
      - Ticket
  /rest/categories:
    post:
      summary: Creates new categories
      description: Creates new categories.
      operationId: postRestCategories
      x-api-path-slug: restcategories-post
      parameters:
      - in: body
        name: /rest/categories
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Categories
  /rest/customer_contracts:
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
  /rest/items:
    post:
      summary: Create new item
      description: Create new item.
      operationId: postRestItems
      x-api-path-slug: restitems-post
      parameters:
      - in: body
        name: /rest/items
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Item
  /rest/items/attributes/markets/maps:
    post:
      summary: Creates a new attribute map.
      description: Creates a new attribute map..
      operationId: postRestItemsAttributesMarketsMaps
      x-api-path-slug: restitemsattributesmarketsmaps-post
      parameters:
      - in: body
        name: /rest/items/attributes/markets/maps
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Attribute
      - Map
  /rest/items/attributes/values/markets/maps:
    post:
      summary: Creates a new attribute value map.
      description: Creates a new attribute value map..
      operationId: postRestItemsAttributesValuesMarketsMaps
      x-api-path-slug: restitemsattributesvaluesmarketsmaps-post
      parameters:
      - in: body
        name: /rest/items/attributes/values/markets/maps
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Attribute
      - Value
      - Map
  /rest/items/{id}/images/upload:
    post:
      summary: Upload a new image
      description: Uploads an image. The item ID must be specified.
      operationId: postRestItemsImagesUpload
      x-api-path-slug: restitemsidimagesupload-post
      parameters:
      - in: body
        name: /rest/items/{id}/images/upload
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Upload
      - New
      - Image
  /rest/languages/translations:
    post:
      summary: Create a new translation
      description: Creates a new translation.
      operationId: postRestLanguagesTranslations
      x-api-path-slug: restlanguagestranslations-post
      parameters:
      - in: query
        name: $fileName
        description: The of the file
      - in: query
        name: $key
        description: The translation key
      - in: query
        name: $languageCode
        description: The language code for the translation
      - in: query
        name: $pluginName
        description: The name of the plugin
      - in: query
        name: $pluginSetId
        description: The ID of the plugin set
      - in: query
        name: $value
        description: The value of the translation
      responses:
        200:
          description: OK
      tags:
      - New
      - Translation
  /rest/listings:
    post:
      summary: Create new listing
      description: Creates a new listing.
      operationId: postRestListings
      x-api-path-slug: restlistings-post
      parameters:
      - in: body
        name: /rest/listings
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Listing
  /rest/listings/layout_templates:
    post:
      summary: Create new layout template
      description: Creates a new layout template.
      operationId: postRestListingsLayoutTemplates
      x-api-path-slug: restlistingslayout-templates-post
      parameters:
      - in: body
        name: /rest/listings/layout_templates
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Layout
      - Template
  /rest/listings/markets:
    post:
      summary: Create new listing market
      description: |-
        Creates a new listing market. Based on the given options this call can create multiple listing markets. If the
        'optionTemplateId' parameter is provided and the listing option template includes options for different markets
        than one listing market will be created for each market.
      operationId: postRestListingsMarkets
      x-api-path-slug: restlistingsmarkets-post
      parameters:
      - in: body
        name: /rest/listings/markets
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Listing
      - Market
  /rest/shop_builder/contents:
    post:
      summary: Create a new content.
      description: Create a new content..
      operationId: postRestShopBuilderContents
      x-api-path-slug: restshop-buildercontents-post
      parameters:
      - in: body
        name: /rest/shop_builder/contents
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Content
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