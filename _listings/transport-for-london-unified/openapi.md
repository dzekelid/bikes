---
swagger: "2.0"
x-collection-name: Transport for London Unified
x-complete: 1
info:
  title: Transport for London Unified
  description: our-unified-api-brings-together-data-across-all-modes-of-transport-into-a-single-restful-api--this-api-provides-access-to-the-most-highly-requested-realtime-and-status-infomation-across-all-the-modes-of-transport-in-a-single-and-consistent-way--access-to-the-developer-documentation-is-available-at-httpsapi-tfl-gov-uk
  version: v1
host: api.tfl.gov.uk
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /BikePoint:
    get:
      summary: Bike Point
      description: "Gets all bike point locations. the place object has an addtionalproperties
        array which contains the nbbikes, nbdocks and nbspaces\r\n            numbers
        which give the status of the bikepoint. a mismatch in these numbers i.e. nbdocks
        - (nbbikes + nbspa."
      operationId: BikePoint_GetAll
      x-api-path-slug: bikepoint-get
      responses:
        200:
          description: OK
      tags:
      - Bike
      - Point
  /BikePoint/Search:
    get:
      summary: Bike Point  Search
      description: "Search for bike stations by their name, a bike point's name often
        contains information about the name of the street\r\n            or nearby
        landmarks, for example. note that the search result does not contain the placeproperties
        i.e. the status\r\n     ."
      operationId: BikePoint_Search
      x-api-path-slug: bikepointsearch-get
      parameters:
      - in: query
        name: query
        description: The search term e
      responses:
        200:
          description: OK
      tags:
      - Bike
      - Point
      - ""
      - Search
  /BikePoint/{id}:
    get:
      summary: Bike Point
      description: Gets the bike point with the given id..
      operationId: BikePoint_Get
      x-api-path-slug: bikepointid-get
      parameters:
      - in: path
        name: id
        description: A bike point id (a list of ids can be obtained from the above
          BikePoint call)
      responses:
        200:
          description: OK
      tags:
      - Bike
      - Point
  /Occupancy/BikePoints/{ids}:
    get:
      summary: Occupancy  Bike Points s
      description: Get the occupancy for bike points..
      operationId: Occupancy_GetBikePointsOccupancies
      x-api-path-slug: occupancybikepointsids-get
      parameters:
      - in: path
        name: ids
      responses:
        200:
          description: OK
      tags:
      - Occupancy
      - ""
      - Bike
      - Points
      - S
---