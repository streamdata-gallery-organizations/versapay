{
  "info": {
    "name": "VersaPay View Batch Details",
    "_postman_id": "1e38edd8-e96b-4ebf-8416-6e644c28e7da",
    "description": "View batch details.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "view",
      "item": [
        {
          "id": "0b184ab9-c5e2-4c16-8f4f-4b132857de69",
          "name": "viewBatchDetail",
          "request": {
            "url": {
              "protocol": "http",
              "host": "secure.versapay.com",
              "path": [
                "api/imports/:id"
              ],
              "variable": [
                {
                  "id": "id",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "View batch details"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "9a0b8f89-54de-4527-89d6-2503e85e5e2e"
            }
          ]
        }
      ]
    }
  ]
}