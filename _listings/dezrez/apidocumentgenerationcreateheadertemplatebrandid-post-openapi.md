---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Uploads a new header template
  version: 1.0.0
  description: Uploads a new header template.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/account/createsystemaccount:
    post:
      summary: Create a new System account eg. new client account
      description: Create a new system account eg. new client account.
      operationId: Account_CreateSystemAccountBydataContract
      x-api-path-slug: apiaccountcreatesystemaccount-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - New
      - System
      - Account
      - Eg
      - ""
      - New
      - Client
      - Account
  /api/agency/savemeetingplace:
    post:
      summary: Saves a new meeting place to that particular agency
      description: Saves a new meeting place to that particular agency.
      operationId: Agency_SaveMeetingPlaceBydataContract
      x-api-path-slug: apiagencysavemeetingplace-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Saves
      - New
      - Meeting
      - Place
      - To
      - That
      - Particular
      - Agency
  /api/auction/savecontact:
    post:
      summary: Add a new contact to the given auction Role or edit an existing contact
      description: Add a new contact to the given auction role or edit an existing
        contact.
      operationId: Auction_SaveAuctionContactBysaveContactDataContract
      x-api-path-slug: apiauctionsavecontact-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: body
        name: saveContactDataContract
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - New
      - Contact
      - To
      - Given
      - Auction
      - Role
      - Edit
      - Existing
      - Contact
  /api/role/auction/milestone/{roleId}:
    post:
      summary: Add a new auction role milestone
      description: Add a new auction role milestone.
      operationId: AuctionRole_AddAuctionMilestoneByroleIdBydataContract
      x-api-path-slug: apiroleauctionmilestoneroleid-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
      responses:
        200:
          description: OK
      tags:
      - New
      - Auction
      - Role
      - Milestone
  /api/cache/List/{listKey}/Append:
    put:
      summary: Adds {itemToAppend} to the tail of an existing list, or creates a new
        list with the object in it.
      description: Adds {itemtoappend} to the tail of an existing list, or creates
        a new list with the object in it..
      operationId: Cache_AppendToListByitemToAppendBylistKeyBytimeToLive
      x-api-path-slug: apicachelistlistkeyappend-put
      parameters:
      - in: body
        name: itemToAppend
        description: The item to append
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: listKey
        description: The list key
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: timeToLive
        description: The time to live
      responses:
        200:
          description: OK
      tags:
      - S
      - ItemToAppend
      - To
      - Tail
      - Of
      - Existing
      - List
      - ""
      - Creates
      - New
      - List
      - Object
      - In
      - It
  /api/cache/List/{listKey}/Prepend:
    put:
      summary: Adds {itemToPrepend} to the head of an existing list, or creates a
        new list with the object in it.
      description: Adds {itemtoprepend} to the head of an existing list, or creates
        a new list with the object in it..
      operationId: Cache_PrependToListByitemToPrependBylistKeyBytimeToLive
      x-api-path-slug: apicachelistlistkeyprepend-put
      parameters:
      - in: body
        name: itemToPrepend
        description: The item to prepend
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: listKey
        description: The list key
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: timeToLive
        description: The time to live
      responses:
        200:
          description: OK
      tags:
      - S
      - ItemToPrepend
      - To
      - Head
      - Of
      - Existing
      - List
      - ""
      - Creates
      - New
      - List
      - Object
      - In
      - It
  /api/chat/savemessage:
    post:
      summary: Save a new chat message.
      description: Save a new chat message..
      operationId: Chat_SaveMessageBychatMessageSave
      x-api-path-slug: apichatsavemessage-post
      parameters:
      - in: body
        name: chatMessageSave
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Save
      - New
      - Chat
      - Message
  /api/chat/message/markasread/{messageId}:
    put:
      summary: This will update the cache with a new timestamp for when this chat
        message was last read.
      description: This will update the cache with a new timestamp for when this chat
        message was last read..
      operationId: Chat_MarkMessageAsReadBymessageId
      x-api-path-slug: apichatmessagemarkasreadmessageid-put
      parameters:
      - in: path
        name: messageId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - This
      - Will
      - Update
      - Cache
      - New
      - Timestampwhen
      - This
      - Chat
      - Message
      - Was
      - Last
      - Read
  /api/digitalsignature/signable/setup/{brandId}/{logoId}/{colour}:
    get:
      summary: creates a new account on signable
      description: Creates a new account on signable.
      operationId: DigitalSignature_SetupBybrandIdBylogoIdBycolourByemailAddress
      x-api-path-slug: apidigitalsignaturesignablesetupbrandidlogoidcolour-get
      parameters:
      - in: path
        name: brandId
        description: brand to associate this sub account to
      - in: path
        name: colour
        description: the web colour to be used in the signable app as a background
          colour, should probably match a logo colour
      - in: query
        name: emailAddress
        description: unique email address for this brand
      - in: path
        name: logoId
        description: logo id used for whitelabelling
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Creates
      - New
      - Account
      - "On"
      - Signable
  /api/documentgeneration/boardordernew:
    post:
      summary: Generates an board ordering New correspondence
      description: Generates an board ordering new correspondence.
      operationId: DocumentGeneration_BoardOrderingNewPackBygeneratePackDetails
      x-api-path-slug: apidocumentgenerationboardordernew-post
      parameters:
      - in: body
        name: generatePackDetails
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Generates
      - Board
      - Ordering
      - New
      - Correspondence
  /api/documentgeneration/createlettertemplate:
    post:
      summary: Uploads a new letter template
      description: Uploads a new letter template.
      operationId: DocumentGeneration_CreateLetterTemplateByletterTemplate
      x-api-path-slug: apidocumentgenerationcreatelettertemplate-post
      parameters:
      - in: body
        name: letterTemplate
        description: The letter template
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Uploads
      - New
      - Letter
      - Template
  /api/documentgeneration/createheadertemplate/{brandId}:
    post:
      summary: Uploads a new header template
      description: Uploads a new header template.
      operationId: DocumentGeneration_CreateHeaderTemplateBybrandIdByletterTemplate
      x-api-path-slug: apidocumentgenerationcreateheadertemplatebrandid-post
      parameters:
      - in: path
        name: brandId
        description: Brand Id for this header
      - in: body
        name: letterTemplate
        description: The letter template
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Uploads
      - New
      - Header
      - Template
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