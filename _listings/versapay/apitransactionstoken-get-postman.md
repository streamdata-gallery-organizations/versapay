{
  "info": {
    "name": "VersaPay View a Transaction",
    "_postman_id": "acc4676d-4eab-437a-9b1b-581907d3e1d7",
    "description": "View a transaction.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "view",
      "item": [
        {
          "id": "027202ef-165a-43ff-866b-cf4d8c308d5d",
          "name": "viewTransaction",
          "request": {
            "url": {
              "protocol": "http",
              "host": "secure.versapay.com",
              "path": [
                "api/transactions/:token"
              ],
              "variable": [
                {
                  "id": "token",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "View a transaction"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b7ee6cd9-efb8-4414-b081-9efa2559d26a"
            }
          ]
        }
      ]
    }
  ]
}