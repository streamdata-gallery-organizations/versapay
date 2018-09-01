{
  "info": {
    "name": "VersaPay Cancel a Transaction",
    "_postman_id": "625fc35c-c54d-4e21-ab0d-fad8f4c343fa",
    "description": "Cancel a `new`, `wait_for_request_approval` or `wait_for_bank_account_verification` transaction you created. Transactions cannot be cancelled after they have been sent to the bank and are `in_progress`.<br>\nAn API key with administrative access is required to approve a transaction.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "cancel",
      "item": [
        {
          "id": "2c95e1cd-0069-40a6-9761-4e40cabb56c3",
          "name": "cancelTransaction",
          "request": {
            "url": {
              "protocol": "http",
              "host": "secure.versapay.com",
              "path": [
                "api/transactions/:token/cancel"
              ],
              "variable": [
                {
                  "id": "token",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Cancel a `new`, `wait_for_request_approval` or `wait_for_bank_account_verification` transaction you created"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8ca66e46-84f1-4202-a96c-3d69b03b45c6"
            }
          ]
        }
      ]
    }
  ]
}