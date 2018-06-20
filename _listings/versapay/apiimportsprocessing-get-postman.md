{
  "info": {
    "name": "VersaPay View In-Progress Batches",
    "_postman_id": "c70ef5fa-8038-4ed5-a5a2-29a5d5238c02",
    "description": "View only recent in-progress import batches.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "view",
      "item": [
        {
          "id": "6b2e2c05-8753-4e53-8db7-1372cd5252f8",
          "name": "viewInProgressBatches",
          "request": {
            "url": "http://secure.versapay.com/api/imports/processing?page=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "View only recent in-progress import batches"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "60aa7470-07e6-43f3-971f-8c1ab00dfbc1"
            }
          ]
        }
      ]
    }
  ]
}