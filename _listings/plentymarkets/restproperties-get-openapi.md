---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets List properties
  description: Lists properties.
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
  /rest/items/properties:
    get:
      summary: List properties
      description: Lists all properties.
      operationId: getRestItemsProperties
      x-api-path-slug: restitemsproperties-get
      parameters:
      - in: query
        name: groupId
        description: Filter restricts the list of results to items linked to a specified
          property group
      - in: query
        name: updatedAt
        description: Filter restricts the list of results to items updated after the
          specified date
      - in: query
        name: with
        description: Includes the specified property information in the results
      responses:
        200:
          description: OK
      tags:
      - List
      - Properties
  /rest/items/variations/variation_properties:
    post:
      summary: Bulk update properties
      description: Creates up to 50 properties of variations.
      operationId: postRestItemsVariationsVariationProperties
      x-api-path-slug: restitemsvariationsvariation-properties-post
      parameters:
      - in: body
        name: /rest/items/variations/variation_properties
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Update
      - Properties
    put:
      summary: Bulk update properties
      description: Updates up to 50 properties of variations.
      operationId: putRestItemsVariationsVariationProperties
      x-api-path-slug: restitemsvariationsvariation-properties-put
      parameters:
      - in: body
        name: /rest/items/variations/variation_properties
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Bulk
      - Update
      - Properties
  /rest/orders/{orderId}/properties/{typeId?}:
    get:
      summary: List properties of an order
      description: Lists properties of an order. The ID of the order must be specified.
      operationId: getRestOrdersOrderPropertiesType
      x-api-path-slug: restordersorderidpropertiestypeid-get
      parameters:
      - in: path
        name: orderId
      - in: query
        name: typeId
        description: The property type ID
      - in: path
        name: typeId?
      responses:
        200:
          description: OK
      tags:
      - List
      - Properties
      - Of
      - Order
  /rest/payments/properties:
    get:
      summary: List properties
      description: List properties.
      operationId: getRestPaymentsProperties
      x-api-path-slug: restpaymentsproperties-get
      parameters:
      - in: query
        name: itemsPerPage
        description: The number of items to list per page
      - in: query
        name: page
        description: The page of results to search for
      responses:
        200:
          description: OK
      tags:
      - List
      - Properties
  /rest/payments/properties/date:
    get:
      summary: List properties by creation date
      description: Lists all properties by creation date. The start and the end of
        the date range must be specified.
      operationId: getRestPaymentsPropertiesDate
      x-api-path-slug: restpaymentspropertiesdate-get
      parameters:
      - in: query
        name: endDate
        description: The end date of the date range for the date of creation of the
          property
      - in: query
        name: itemsPerPage
        description: The number of items to list per page
      - in: query
        name: page
        description: The page of results to search for
      - in: query
        name: startDate
        description: The start date of the date range for the date of creation of
          the property
      responses:
        200:
          description: OK
      tags:
      - List
      - Properties
      - By
      - Creation
      - Date
  /rest/properties:
    get:
      summary: List properties
      description: Lists properties.
      operationId: getRestProperties
      x-api-path-slug: restproperties-get
      responses:
        200:
          description: OK
      tags:
      - List
      - Properties
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