---
swagger: "2.0"
x-collection-name: PayRun
x-complete: 0
info:
  title: Pay Run.IO Insert new auto enrolment assessment
  description: Creates a new auto enrolment assessment for the employee. Used to insert
    historical assessments
  version: 17.18.6.206
host: api.test.payrun.io
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Employer/{EmployerId}/Employee/{EmployeeId}/AEAssessment/{AEAssessmentId}:
    put:
      summary: Insert new auto enrolment assessment
      description: Creates a new auto enrolment assessment for the employee. Used
        to insert historical assessments
      operationId: PutNewAEAssessment
      x-api-path-slug: employeremployeridemployeeemployeeidaeassessmentaeassessmentid-put
      parameters:
      - in: body
        name: AEAssessment
        description: The auto enrolment assessment object
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: AEAssessmentId
        description: The auto enrolment assessment unique identifier
      - in: header
        name: Api-Version
        description: The version of the api to target
      - in: header
        name: Authorization
        description: The OAuth 1 authorization header
      - in: path
        name: EmployeeId
        description: The employees unique identifier
      - in: path
        name: EmployerId
        description: The employers unique identifier
      responses:
        200:
          description: OK
      tags:
      - Insert
      - New
      - Auto
      - Enrolment
      - Assessment
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