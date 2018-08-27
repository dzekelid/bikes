{
  "info": {
    "name": "Coord Bike Share API Get bike locations in the requested search area, as a GeoJSON FeatureCollection.",
    "_postman_id": "09a7264e-05f2-433e-9467-a7b3cdbae3b5",
    "description": "Get a list of locations given the input parameters. Specify a search area by radius around\na latitude and longitude, as well as any filter for specific systems. Each location will\nbe a GeoJSON Feature, and aggregated into a GeoJSON FeatureCollection.\n\n### Example\n\n#### Request:\n`curl -G \"https://api.coord.co/v1/bike/location?latitude=40.742868&longitude=-73.989186&radius_km=0.25&access_key=\"`\n\n#### Response:\n```\n{\n  \"features\": [\n    {\n      \"geometry\": {\n        \"coordinates\": [\n          -73.98918628692627,\n          40.74286877312112\n        ],\n        \"type\": \"Point\"\n      },\n      \"id\": \"CitiBike-3641\",\n      \"properties\": {\n        \"is_renting\": true,\n        \"is_returning\": true,\n        \"last_reported\": \"2018-05-17T15:39:24.000Z\",\n        \"lat\": 40.74286877312112,\n        \"location_id\": \"3641\",\n        \"location_type\": \"bike_station_dock\",\n        \"lon\": -73.98918628692627,\n        \"name\": \"Broadway & W 25 St\",\n        \"num_bikes_available\": 53,\n        \"num_docks_available\": 1,\n        \"region_id\": \"71\",\n        \"system_id\": \"CitiBike\"\n      },\n      \"type\": \"Feature\"\n    },\n    {\n      \"geometry\": {\n        \"coordinates\": [\n          -73.99144871,\n          40.74395411\n        ],\n        \"type\": \"Point\"\n      },\n      \"id\": \"CitiBike-466\",\n      \"properties\": {\n        \"is_renting\": true,\n        \"is_returning\": true,\n        \"last_reported\": \"2018-05-17T15:32:40.000Z\",\n        \"lat\": 40.74395411,\n        \"location_id\": \"466\",\n        \"location_type\": \"bike_station_dock\",\n        \"lon\": -73.99144871,\n        \"name\": \"W 25 St & 6 Ave\",\n        \"num_bikes_available\": 35,\n        \"region_id\": \"71\",\n        \"system_id\": \"CitiBike\"\n      },\n      \"type\": \"Feature\"\n    }\n  ],\n  \"type\": \"FeatureCollection\"\n}\n```",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Bike",
      "item": [
        {
          "id": "68c85b02-20cb-42fd-a019-0c498425bdcf",
          "name": "search_locations",
          "request": {
            "url": "http://api.coord.co/v1/bike/location?access_key=%7B%7D&latitude=%7B%7D&longitude=%7B%7D&radius_km=%7B%7D&system_ids=%7B%7D",
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Get a list of locations given the input parameters. Specify a search area by radius around\na latitude and longitude, as well as any filter for specific systems. Each location will\nbe a GeoJSON Feature, and aggregated into a GeoJSON FeatureCollection.\n\n### Example\n\n#### Request:\n`curl -G \"https://api.coord.co/v1/bike/location?latitude=40.742868&longitude=-73.989186&radius_km=0.25&access_key=\"`\n\n#### Response:\n```\n{\n  \"features\": [\n    {\n      \"geometry\": {\n        \"coordinates\": [\n          -73.98918628692627,\n          40.74286877312112\n        ],\n        \"type\": \"Point\"\n      },\n      \"id\": \"CitiBike-3641\",\n      \"properties\": {\n        \"is_renting\": true,\n        \"is_returning\": true,\n        \"last_reported\": \"2018-05-17T15:39:24.000Z\",\n        \"lat\": 40.74286877312112,\n        \"location_id\": \"3641\",\n        \"location_type\": \"bike_station_dock\",\n        \"lon\": -73.98918628692627,\n        \"name\": \"Broadway & W 25 St\",\n        \"num_bikes_available\": 53,\n        \"num_docks_available\": 1,\n        \"region_id\": \"71\",\n        \"system_id\": \"CitiBike\"\n      },\n      \"type\": \"Feature\"\n    },\n    {\n      \"geometry\": {\n        \"coordinates\": [\n          -73.99144871,\n          40.74395411\n        ],\n        \"type\": \"Point\"\n      },\n      \"id\": \"CitiBike-466\",\n      \"properties\": {\n        \"is_renting\": true,\n        \"is_returning\": true,\n        \"last_reported\": \"2018-05-17T15:32:40.000Z\",\n        \"lat\": 40.74395411,\n        \"location_id\": \"466\",\n        \"location_type\": \"bike_station_dock\",\n        \"lon\": -73.99144871,\n        \"name\": \"W 25 St & 6 Ave\",\n        \"num_bikes_available\": 35,\n        \"region_id\": \"71\",\n        \"system_id\": \"CitiBike\"\n      },\n      \"type\": \"Feature\"\n    }\n  ],\n  \"type\": \"FeatureCollection\"\n}\n```"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "5a9fd451-ff0e-4d16-bc51-90a02407df6b"
            }
          ]
        }
      ]
    }
  ]
}