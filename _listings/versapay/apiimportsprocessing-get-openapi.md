---
swagger: "2.0"
x-collection-name: VersaPay
x-complete: 0
info:
  title: VersaPay View In-Progress Batches
  description: View only recent in-progress import batches.
  contact:
    name: VersaPay Support
    url: https://www.versapay.com/support
    email: support@versapay.com
  version: 1.0.0
host: secure.versapay.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/funds:
    get:
      summary: View Your Fund Sources
      description: View your fund sources.
      operationId: getFundSources
      x-api-path-slug: apifunds-get
      responses:
        200:
          description: OK
      tags:
      - View
      - Your
      - Fund
      - Sources
  /api/transactions:
    get:
      summary: View Transactions
      description: View transactions.
      operationId: viewAllTransactions
      x-api-path-slug: apitransactions-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - ""
      - Transactionss
    post:
      summary: Create Transactions
      description: Create transactions.
      operationId: createTransaction
      x-api-path-slug: apitransactions-post
      parameters:
      - in: body
        name: body
        description: Transaction to create
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - ""
      - Transactionss
  /api/transactions/{token}:
    get:
      summary: View a Transaction
      description: View a transaction.
      operationId: viewTransaction
      x-api-path-slug: apitransactionstoken-get
      parameters:
      - in: path
        name: token
        description: The transaction identifier
      responses:
        200:
          description: OK
      tags:
      - View
      - Transactions
  /api/transactions/{token}/approve:
    post:
      summary: Approve a Transaction
      description: |-
        Approve a `new` or `wait_for_request_approval` transaction.<br>
        An API key with administrative access is required to approve a transaction.
      operationId: approveTransaction
      x-api-path-slug: apitransactionstokenapprove-post
      parameters:
      - in: body
        name: fund_token
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: token
        description: The transaction identifier
      responses:
        200:
          description: OK
      tags:
      - Approve
      - Transactions
  /api/transactions/{token}/cancel:
    post:
      summary: Cancel a Transaction
      description: |-
        Cancel a `new`, `wait_for_request_approval` or `wait_for_bank_account_verification` transaction you created. Transactions cannot be cancelled after they have been sent to the bank and are `in_progress`.<br>
        An API key with administrative access is required to approve a transaction.
      operationId: cancelTransaction
      x-api-path-slug: apitransactionstokencancel-post
      parameters:
      - in: path
        name: token
        description: The transaction identifier
      responses:
        200:
          description: OK
      tags:
      - Cancel
      - Transactions
  /api/debit_agreements:
    post:
      summary: Create an Agreement
      description: Create an agreement.
      operationId: createAgreement
      x-api-path-slug: apidebit-agreements-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Create
      - ""
      - Agreementss
  /api/debit_agreements/sent:
    get:
      summary: View Sent Agreements
      description: View sent agreements.
      operationId: viewSentAgreements
      x-api-path-slug: apidebit-agreementssent-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - Sent
      - Agreements
  /api/debit_agreements/received:
    get:
      summary: View Received Agreements
      description: View received agreements.
      operationId: viewReceivedAgreements
      x-api-path-slug: apidebit-agreementsreceived-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - Received
      - Agreements
  /api/debit_agreements/{token}/approve:
    post:
      summary: Approve an Agreement
      description: Approve an agreement.
      operationId: approveAgreement
      x-api-path-slug: apidebit-agreementstokenapprove-post
      parameters:
      - in: body
        name: fund_token
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Approve
      - Agreements
  /api/debit_agreements/{token}/cancel:
    post:
      summary: Cancel an Agreement
      description: Cancel an agreement.
      operationId: cancelAgreement
      x-api-path-slug: apidebit-agreementstokencancel-post
      parameters:
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Cancel
      - Agreements
  /api/debit_agreements/{token}/reject:
    post:
      summary: Reject an Agreement
      description: Reject a *pending* agreement by supplying an agreement's *token*
        attribute and providing a *rejection_reason*.
      operationId: rejectAgreement
      x-api-path-slug: apidebit-agreementstokenreject-post
      parameters:
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Reject
      - Agreements
  /api/debit_agreements/{token}/revoke:
    post:
      summary: Revoke an Agreement
      description: Revoke an *approved* agreement for your account by supplying an
        agreement's token attribute. The agreement's creator will no longer be able
        to debit your account using this agreement.
      operationId: revokeAgreement
      x-api-path-slug: apidebit-agreementstokenrevoke-post
      parameters:
      - in: path
        name: token
        description: The agreement identifier
      responses:
        200:
          description: OK
      tags:
      - Revoke
      - Agreements
  /send_money:
    get:
      summary: Single Payment Hosted Checkout
      description: |-
        Clients, customers, or donors, for instance, can send your organization money directly from their bank account or credit card simply by clicking a link which displays a page with your account name allowing your customer to make a payment to you for the specified dollar amount:
        <br>
        `https://secure.versapay.com/send_money?api_token={your_api_token}&amount={dollar_amount_for_customer_to_pay}`
        <br>
        Funds will go to the fund destination passed in the to_fund parameter. By default, the funds will be deposited into your default bank account once the transaction clears from the other party.
      operationId: hostedCheckout
      x-api-path-slug: send-money-get
      parameters:
      - in: query
        name: amount
        description: The amount in dollars that the transaction is for
      - in: query
        name: api_token
        description: A valid API token generated from your account
      - in: query
        name: link_url
        description: A url that gets stored and displayed on the transaction for an
          invoice
      - in: query
        name: locale
        description: Set the default language of the checkout, either `en` or `fr`
      - in: query
        name: message
        description: A message which will be stored with the transaction
      - in: query
        name: pref
        description: The preferred payment type either `ba` or `cc` for bank or credit
          card respectively
      - in: query
        name: reference
        description: Extra data (max 255 characters)
      - in: query
        name: return_to
        description: A url which will displayed to the user to return to your website
          after they finish the Signup and Confirmation
      - in: query
        name: to_fund
        description: The token of the bank account or balance where the funds should
          go to
      responses:
        200:
          description: OK
      tags:
      - Single
      - Payment
      - Hosted
      - Checkout
  /authorize:
    get:
      summary: Debit Agreement Hosted Checkout
      description: |-
        Clients, customers, or donors, for instance, can initiate a pre-authorized debit agreement by clicking a link on your website or in an email.
        <br>
        `https://secure.versapay.com/authorize?api_token={your_api_token}&message={explanation_of_what_this_is_for}`
        <br>
      operationId: clients-customers-or-donors-for-instance-can-initiate-a-preauthorized-debit-agreement-by-clicking-a-
      x-api-path-slug: authorize-get
      parameters:
      - in: query
        name: api_token
        description: A valid API token generated from your account
      - in: query
        name: message
        description: A message for the user describing the pre-authorized debit agreement
      - in: query
        name: reference
        description: Extra data (max 255 characters)
      - in: query
        name: return_to
        description: A url which will displayed to the user to return to your website
          after they finish the Signup and Confirmation
      responses:
        200:
          description: OK
      tags:
      - Debit
      - ""
      - Agreements
      - Hosted
      - Checkout
  /api/imports/customer:
    post:
      summary: Create and Update Customer
      description: |-
        Create a customer in ARC using the following attributes (at minimum by providing values for required attributes). If providing an identifier for an existing customer, its information is updated.<br><br>
        *Note: Any additional non-standard attribute will be stored with customer record and available for presentment rendering.*
      operationId: createCustomer
      x-api-path-slug: apiimportscustomer-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Customer
  /api/imports/invoice:
    post:
      summary: Create and Update Invoice
      description: |-
        Create and update invoices in ARC. If the invoice already exists when a request is processed, it will be updated.<br><br>
        The set of attributes to send in the request body may vary based on the account configuration. Please contact the implementation specialist for more information.<br><br>
        *Note:*
          * *Customer will be created/updated using the customer_&ast; attributes if necessary at time of invoice import.*
          * *Any additional non-standard attribute will be stored with invoice record and available for presentment rendering.*
      operationId: createInvoice
      x-api-path-slug: apiimportsinvoice-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Invoice
  /api/imports/payment:
    post:
      summary: Create a Payment
      description: "Create and update external payment records in ARC.<br><br>The
        set of attributes to send in the request body may vary based on the account
        configuration. Please contact the implementation specialist for more information.<br><br>\nThe
        request schema for posting a payment for a single invoice is slightly different
        than that for posting a payment for multiple invoices.\n\nFor instance, sample
        request for posting payment for a single invoice looks like:\n```\n{\n  \"identifier\":
        \"PMT0010-05\",\n  \"invoice_number\": \"INV1234-01\",\n  \"amount\": 10000,\n
        \ \"currency\": \"usd\",\n  \"date\": \"2018-01-10\",\n  \"customer_identifier\":
        \"C1234\",\n  \"customer_name\": \"Acme Inc.\",\n  \"notes\": \"Notes\",\n
        \ \"ref1\": \"1234\",\n  \"ref2\": \"PO# 84767\"\n}\n```\n\n*Note: Customer
        will be created using the customer_&ast; attributes if it doesn\u2019t already
        exist at the time of payment import.*"
      operationId: createPayment
      x-api-path-slug: apiimportspayment-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - CreatePayment
  /api/imports:
    get:
      summary: View In-Progress & Completed Batches
      description: View recent in-progress and completed import batches.
      operationId: viewAllBatches
      x-api-path-slug: apiimports-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - In-Progress
      - '&'
      - Completed
      - Batches
    post:
      summary: Import a CSV File
      description: "When uploading a CSV-formatted file it\u2019s helpful to use your
        language/framework tooling to simplify the [multipart/form-data](https://www.ietf.org/rfc/rfc2388.txt)
        file upload.\n### Size Limit\nThe file cannot exceed 25MB.\n### Layouts\nPlease
        contact support@versapay.com or reach out to your implementation specialist
        for standard inbound CSV file layouts."
      operationId: importBatchFile
      x-api-path-slug: apiimports-post
      parameters:
      - in: formData
        name: file
        description: The file to upload
      - in: formData
        name: filename
        description: Name of original file
      responses:
        200:
          description: OK
      tags:
      - ImportCSV
      - File
  /api/imports/processing:
    get:
      summary: View In-Progress Batches
      description: View only recent in-progress import batches.
      operationId: viewInProgressBatches
      x-api-path-slug: apiimportsprocessing-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - In-Progress
      - Batches
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---