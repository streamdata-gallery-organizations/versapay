---
swagger: "2.0"
x-collection-name: VersaPay
x-complete: 1
info:
  title: VersaPay API Reference
  description: -introductionthe-versapay-api-offers-operations-in-support-of-its-flagship-products-arc--accounts-receivable-platform-with-automated-invoicing-effective-collaboration-flexible-payments-and-cash-application-to-improve-efficiency-and-customer-relationships----importing--exporting-customers-invoices-and-payments----monitoring-file-based-importsbatches--payport--cloud-based-platform-to-electronically-push-and-pull-funds-across-the-eft--ach-network----moving-funds-using-transactions-and-preauthorized-debit-agreements----a-secure-hosted-checkout-for-accepting-payments-through-your-website-or-email-please-contact-us-at-supportversapay-com-for-support--setup-of-ar-invoicing-integration-hosted-checkout-andor-payment-acceptance--environmentsthe-demo-environment-is-a-useful-sandbox-for-integration-testing-where-transaction-settlements-are-simulated-using-test-account-numbers-and-test-dollar-amounts-httpsdemo-versapay-comonce-integration-testing-is-complete-via-the-demo-environment-start-sending-your-requests-to-the-production-url-to-start-moving-money-andor-integrating-with-versapay-httpssecure-versapay-com-rate-limitsthere-is-a-60-request-per-minute-api-limit--any-requests-above-this-limit-will-result-in-http-return-code-403-forbidden-rate-limit-exceeded--access-to-api-keysvisit-your-account-settings-in-demohttpsdemo-versapay-comaccount-or-productionhttpssecure-versapay-comaccount-to-setup-api-keys-needed-for-authentication-as-well-as-webhooks-to-receive-relevant-callbacks-from-versapay-transaction-processing--you-can-generatedisable-your-api-keys-as-often-as-necessary-for-security-reasons-if-you-do-not-have-an-account-please-contact-versapay-support-for-support--setup-of-ar-invoicing-integration-hosted-checkout-andor-payment-acceptance--authenticationapi-requests-are-authenticated-using-http-basic-access-authenticationhttpsen-wikipedia-orgwikibasic-access-authentication--simply-provide-the-tokenkey-values-as-the-user-and-password-parameters-using-curl-for-instancecurl-u-nvax---un0i----x-post-httpssecure-versapay-comapi----testing-transactions-eft-bank-account-numbersin-the-demo-environment-the-following-test-bank-accounts-can-be-setup-up-in-your-account-institutioninstitution-numberbranchaccount-numbertd00499960112-digitsrbc00316824112-digitsbmo00199520112-digitshsbc01610880112-digitswhen-versapay-prompts-you-to-verify-these-bank-accounts-enter-a-value-of-1-23-for-the-verification-amount-to-determine-the-outcome-of-a-transaction-funded-by-a-bank-account-set-the-amount-accordinglyamountresulting-statex-10nsfedx-11completed-but-nsfedx-30erroranything-elsecompleted-ach-bank-account-numbersplease-contact-supportversapay-com-for-support--setup-of-ach-acceptance-and-bank-account-numbers-that-can-be-used-for-testing--credit-card-numbersplease-contact-supportversapay-com-for-support--setup-of-credit-card-acceptance-and-card-brandsnumbers-that-can-be-used-for-testing--tools-postmantry-out-the-api-using-postman-apphttpswww-getpostman-com-a-powerful-rest-api-client--download-the-versapay-api-reference-as-a-postman-collection-by-clicking-on-the-button-belowrun-in-postmanhttpsrun-pstmn-iobutton-svghttpsapp-getpostman-comruncollection7e34e0700a2f8c3074c6after-downloading-the-collection-set-up-and-configure-the-environment-as-follows1--download-the-sample-environment-filehttpsdevelopers-versapay-comdemo-postman-environment-json-2--import-the-environment-file-in-postman---import-environmenthttpsdevelopers-versapay-comimagesimport-environment-png3--once-it-is-imported-edit-the-environment-to-add-api-token-and-keys-associated-to-your-test-account---edit-environmenthttpsdevelopers-versapay-comimagesedit-environment-png4--click-update-to-save-your-changes-5--before-placing-api-calls-make-sure-the-correct-environment-is-selected---select-environmenthttpsdevelopers-versapay-comimagesselect-environment-png
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
  /api/imports/completed:
    get:
      summary: View Completed Batches
      description: View only recent completed import batches.
      operationId: viewCompletedBatches
      x-api-path-slug: apiimportscompleted-get
      parameters:
      - in: query
        name: page
        description: 50 items are displayed per page
      responses:
        200:
          description: OK
      tags:
      - View
      - Completed
      - Batches
  /api/imports/{id}:
    get:
      summary: View Batch Details
      description: View batch details.
      operationId: viewBatchDetail
      x-api-path-slug: apiimportsid-get
      parameters:
      - in: path
        name: id
        description: The import batch identifier
      responses:
        200:
          description: OK
      tags:
      - View
      - Batch
      - Details
  /api/exports/payment_amounts:
    get:
      summary: Payments made in ARC
      description: Payments made to your supplier account from your customers since
        watermark, limited to 100 payment amounts at a time.<br><br>A consumer should
        store the last `id` value of each response and include it as the watermark
        parameter for a subsequent calls.
      operationId: getARCPayments
      x-api-path-slug: apiexportspayment-amounts-get
      parameters:
      - in: query
        name: watermark
        description: The `id` value to base a subsequent extract of the next 100 payment
          amounts
      responses:
        200:
          description: OK
      tags:
      - Payments
      - made
      - in
      - ARC
  /api/exports/disputes:
    get:
      summary: Open and Closed Disputes
      description: Open and closed disputes since watermark, limited to 100 disputes
        at a time.
      operationId: getDisputes
      x-api-path-slug: apiexportsdisputes-get
      parameters:
      - in: query
        name: watermark
        description: The date value to base a subsequent extract of the next 100 disputes
      responses:
        200:
          description: OK
      tags:
      - OpenClosed
      - Disputes
---