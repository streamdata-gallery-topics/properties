---
swagger: "2.0"
x-collection-name: ATTOM
x-complete: 0
info:
  title: Attom Data Solutions API Returns properties and their characteristics that
    fit a criteria.
  description: Get a list of property snapshots within a specific city that are within
    a desired size range and a specific property type.
  version: 1.0.0
host: search.onboard-apis.com
basePath: /communityapi/v2.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /property/id:
    get:
      summary: Returns a list of properties that fit a criteria.
      description: Get a list of property IDs within a specific geography that have
        a specific number of beds. Use orderby to choose how you want your results
        sorted.
      operationId: getPropertyIdList
      x-api-path-slug: propertyid-get
      parameters:
      - in: header
        name: accept
        description: application/xml or application/json (default)
      - in: header
        name: apikey
        description: Application Key
      - in: query
        name: geoid
        description: A list of geographies that this property belongs to
      - in: query
        name: maxBeds
        description: The max Bed size to search from
      - in: query
        name: minBeds
        description: The min Bed size to search from
      - in: query
        name: orderby
        description: Sort Options
      responses:
        200:
          description: OK
      tags:
      - Returns
      - List
      - Of
      - Properties
      - That
      - Fit
      - Criteria
  /property/address:
    get:
      summary: Returns properties within a zip code.
      description: Get a list of properties within a zip code. Use propertytype and
        order by to narrow down your results.
      operationId: adressList
      x-api-path-slug: propertyaddress-get
      parameters:
      - in: header
        name: accept
        description: application/xml or application/json (default)
      - in: query
        name: address1
        description: The first line of the mailing address
      - in: query
        name: address2
        description: The second line of the mailing address
      - in: header
        name: apikey
        description: Application Key
      - in: query
        name: orderby
        description: Sorting Options
      - in: query
        name: page
        description: The current view index based on the pagesize and the total number
          of records available
      - in: query
        name: pagesize
        description: The number of records to be returned with the request
      - in: query
        name: postalcode
        description: The zip code or postal code to search
      - in: query
        name: propertytype
        description: A specific property classification such as Detached Single Family
      - in: query
        name: radius
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Properties
      - Within
      - Zip
      - Code
  /property/snapshot:
    get:
      summary: Returns properties and their characteristics that fit a criteria.
      description: Get a list of property snapshots within a specific city that are
        within a desired size range and a specific property type.
      operationId: propertySnapshot
      x-api-path-slug: propertysnapshot-get
      parameters:
      - in: header
        name: accept
        description: application/xml or application/json (default)
      - in: header
        name: apikey
        description: Application Key
      - in: query
        name: cityname
        description: The name of the city to search from
      - in: query
        name: latitude
        description: The property latitude coordinate
      - in: query
        name: longitude
        description: The property longitude coordinate
      - in: query
        name: maxavmvalue
        description: The maximum AVM Valuey
      - in: query
        name: maxLotSize1
        description: The max Lot size 1 to search from
      - in: query
        name: maxtaxamt
        description: The total amount of taxes paid to the local taxing authority
      - in: query
        name: minavmvalue
        description: The minimum AVM Value
      - in: query
        name: minLotSize1
        description: The min Lot size 1 to search from
      - in: query
        name: mintaxamt
        description: The total amount of taxes paid to the local taxing authority
      - in: query
        name: orderby
        description: Sorting Options
      - in: query
        name: postalcode
      - in: query
        name: propertytype
        description: A specific property classification such as Detached Single Family
      - in: query
        name: radius
      responses:
        200:
          description: OK
      tags:
      - Returns
      - Properties
      - Their
      - Characteristics
      - That
      - Fit
      - Criteria
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