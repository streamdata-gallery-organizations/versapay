{
  "info": {
    "name": "VersaPay View Completed Batches",
    "_postman_id": "7a6bac1c-489f-4b11-b691-49f558fdba12",
    "description": "View only recent completed import batches.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "view",
      "item": [
        {
          "id": "85f6db84-5e86-4e29-8d58-b9cf5704253b",
          "name": "viewCompletedBatches",
          "request": {
            "url": "http://secure.versapay.com/api/imports/completed?page=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "View only recent completed import batches"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "62b68306-ba95-4dd0-a492-eba54235b1d6"
            }
          ]
        }
      ]
    }
  ]
}