{
  "info": {
    "name": "VersaPay View Transactions",
    "_postman_id": "6dd58e13-e892-4a60-a604-e4e3181ddf9e",
    "description": "View transactions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "view",
      "item": [
        {
          "id": "7cc56372-dd39-4de1-9319-ff14908f7bb3",
          "name": "viewAllTransactions",
          "request": {
            "url": "http://secure.versapay.com/api/transactions?page=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "View transactions"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "c0e4bb4a-b786-4a0a-8aa0-3a329c7be729"
            }
          ]
        }
      ]
    }
  ]
}