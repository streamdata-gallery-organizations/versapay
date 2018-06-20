{
  "info": {
    "name": "VersaPay View Your Fund Sources",
    "_postman_id": "258ecd52-a297-4bb3-be55-72a6fe93985d",
    "description": "View your fund sources.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "view",
      "item": [
        {
          "id": "01495286-7da6-49c6-bfc8-808a13772721",
          "name": "getFundSources",
          "request": {
            "url": "http://secure.versapay.com/api/funds",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "View your fund sources"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7b2d3c9b-6564-4f77-8c52-d9099b5a2a34"
            }
          ]
        }
      ]
    }
  ]
}