---
swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 0
info:
  title: Geo Mark Web Service Create a new geomark
  description: Create a new geomark from the geometries read from the 'body' parameter
    or file.
  termsOfService: http://www2.gov.bc.ca/gov/content/governments/about-the-bc-government/databc/open-data/api-terms-of-use-for-ogl-information
  contact:
    name: Data BC
    url: http://data.gov.bc.ca/
    email: DataBCBA@gov.bc.ca
  version: 4.1.2
host: apps.gov.bc.ca
basePath: /pub/geomark
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /geomarks/new:
    post:
      summary: Create a new geomark
      description: Create a new geomark from the geometries read from the 'body' parameter
        or file.
      operationId: create-a-new-geomark-from-the-geometries-read-from-the-body-parameter-or-file-
      x-api-path-slug: geomarksnew-post
      parameters:
      - in: formData
        name: body
        description: The binary or character content representing the geometry or
          geometries
      - in: formData
        name: bufferCap
        description: If bufferMetres is specified, The style of buffer to use at the
          ends of a buffered line
      - in: formData
        name: bufferJoin
        description: If bufferMetres is specified, The style of buffer to use for
          joins between the line segments for lines and polygons
      - in: formData
        name: bufferMetres
        description: The amount to buffer the geometry in metres, must only contain
          numerical digits (e
      - in: formData
        name: bufferMitreLimit
        description: If bufferMetres is specified, the maximum ratio of distance from
          the original geometry to a mitre buffer point and the buffer amount
      - in: formData
        name: bufferSegments
        description: If bufferMetres is specified, the number of line segments used
          in each quadrant to approximate the curve for round end-cap and join styles
      - in: formData
        name: callback
        description: The callback function a JSON result format would be wrapped in
          to support Ajax requests
      - in: formData
        name: failureRedirectUrl
        description: The url to redirect if the geomark could not be created
      - in: formData
        name: format
        description: The file format name extension of the input geometry
      - in: formData
        name: multiple
        description: Boolean flag indicating if multiple geometries are to be used
          for the geomark (true) or only a single geometry from the first geometry
          (false)
      - in: formData
        name: redirectUrl
        description: The optional external URL to redirect the user to when the geomark
          is created rather than showing the geomark info page
      - in: formData
        name: resultFormat
        description: The file format the geomark info resource should be returned
          using
      - in: formData
        name: srid
        description: The srid of the coordinate system the input geometries are in
      responses:
        200:
          description: OK
      tags:
      - Geomarks
      - New
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