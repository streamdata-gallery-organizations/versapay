---
swagger: "2.0"
x-collection-name: VersaPay
x-complete: 0
info:
  title: VersaPay Revoke an Agreement
  description: Revoke an *approved* agreement for your account by supplying an agreement's
    token attribute. The agreement's creator will no longer be able to debit your
    account using this agreement.
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