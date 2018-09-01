{
  "info": {
    "name": "VersaPay Import a CSV File",
    "_postman_id": "5a25e608-d92c-416c-87e2-56a21920744d",
    "description": "When uploading a CSV-formatted file it???s helpful to use your language/framework tooling to simplify the [multipart/form-data](https://www.ietf.org/rfc/rfc2388.txt) file upload.\n### Size Limit\nThe file cannot exceed 25MB.\n### Layouts\nPlease contact support@versapay.com or reach out to your implementation specialist for standard inbound CSV file layouts.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "importcsv",
      "item": [
        {
          "id": "8263cd8c-8559-45f3-9262-606fcc0c86d6",
          "name": "importBatchFile",
          "request": {
            "url": "http://secure.versapay.com/api/imports",
            "method": "POST",
            "body": {
              "mode": "urlencoded",
              "urlencoded": [
                {
                  "key": "file",
                  "value": "{}",
                  "disabled": false,
                  "description": "The file to upload"
                },
                {
                  "key": "filename",
                  "value": "{}",
                  "disabled": false,
                  "description": "Name of original file"
                }
              ]
            },
            "description": "When uploading a CSV-formatted file it???s helpful to use your language/framework tooling to simplify the [multipart/form-data](https://www"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "31b7011b-fff1-4566-8feb-b43270fc70b6"
            }
          ]
        }
      ]
    }
  ]
}