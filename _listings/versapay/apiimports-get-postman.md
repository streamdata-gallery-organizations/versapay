{
  "info": {
    "name": "VersaPay View In-Progress & Completed Batches",
    "_postman_id": "6b8a52fb-31a0-4698-9212-9a2b0f0e24b0",
    "description": "View recent in-progress and completed import batches.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "view",
      "item": [
        {
          "id": "96dc2940-3bd5-446d-b461-6110e33af5b9",
          "name": "viewAllBatches",
          "request": {
            "url": "http://secure.versapay.com/api/imports?page=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "View recent in-progress and completed import batches"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8caea03-2ba2-4ffd-b3e7-b78a7ab8341d"
            }
          ]
        }
      ]
    }
  ]
}