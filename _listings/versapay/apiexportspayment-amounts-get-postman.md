{
  "info": {
    "name": "VersaPay Payments made in ARC",
    "_postman_id": "73bcd0eb-d5ad-4ec7-ad36-e07b7bb7b739",
    "description": "Payments made to your supplier account from your customers since watermark, limited to 100 payment amounts at a time.<br><br>A consumer should store the last `id` value of each response and include it as the watermark parameter for a subsequent calls.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "payments",
      "item": [
        {
          "id": "8577db1a-96bd-4149-b501-d1e4d95e8695",
          "name": "getARCPayments",
          "request": {
            "url": "http://secure.versapay.com/api/exports/payment_amounts?watermark=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Payments made to your supplier account from your customers since watermark, limited to 100 payment amounts at a time"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b803472d-b9cc-4959-8cfc-61b22f1a58c4"
            }
          ]
        }
      ]
    }
  ]
}