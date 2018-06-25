---
name: VersaPay
x-slug: versapay
description: VersaPay handles elements of both credit and debit card merchant payment
  processing in Canada. In offering a host of merchant account services and credit
  card POS terminals it allows for an efficient merchant payment service in all aspects-
  in person, on the go, online, and at the office. Founded in 2005 by Michael Gokturk,
  VersaPay is a Canadian owned and operated national financial transaction services
  provider partnered with Chase Paymentech. Versapay also offers electronic funds
  transfer through a system called Versapay EMT.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
x-kinRank: "9"
x-alexaRank: "410909"
tags: VersaPay
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apis.md
specificationVersion: "0.14"
apis:
- name: VersaPay View Your Fund Sources
  x-api-slug: versapay
  description: View your fund sources.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/funds
  tags: View, Your, Fund, Sources
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apifunds-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apifunds-get-openapi.md
- name: VersaPay View Transactions
  x-api-slug: versapay
  description: View transactions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/transactions
  tags: View, ,Transactionss
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactions-get-openapi.md
- name: VersaPay Create Transactions
  x-api-slug: versapay
  description: Create transactions.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/transactions
  tags: ',Transactionss'
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactions-post-openapi.md
- name: VersaPay View a Transaction
  x-api-slug: versapay
  description: View a transaction.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/transactions/{token}
  tags: View,Transactions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactionstoken-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactionstoken-get-openapi.md
- name: VersaPay Approve a Transaction
  x-api-slug: versapay
  description: |-
    Approve a `new` or `wait_for_request_approval` transaction.<br>
    An API key with administrative access is required to approve a transaction.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/transactions/{token}/approve
  tags: Approve,Transactions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactionstokenapprove-post-openapi.md
- name: VersaPay Cancel a Transaction
  x-api-slug: versapay
  description: |-
    Cancel a `new`, `wait_for_request_approval` or `wait_for_bank_account_verification` transaction you created. Transactions cannot be cancelled after they have been sent to the bank and are `in_progress`.<br>
    An API key with administrative access is required to approve a transaction.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/transactions/{token}/cancel
  tags: Cancel,Transactions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactionstokencancel-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apitransactionstokencancel-post-openapi.md
- name: VersaPay Create an Agreement
  x-api-slug: versapay
  description: Create an agreement.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/debit_agreements
  tags: Create,,Agreementss
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreements-post-openapi.md
- name: VersaPay View Sent Agreements
  x-api-slug: versapay
  description: View sent agreements.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/debit_agreements/sent
  tags: View, Sent,Agreements
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementssent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementssent-get-openapi.md
- name: VersaPay View Received Agreements
  x-api-slug: versapay
  description: View received agreements.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/debit_agreements/received
  tags: View, Received,Agreements
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementsreceived-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementsreceived-get-openapi.md
- name: VersaPay Approve an Agreement
  x-api-slug: versapay
  description: Approve an agreement.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/debit_agreements/{token}/approve
  tags: Approve,Agreements
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementstokenapprove-post-openapi.md
- name: VersaPay Cancel an Agreement
  x-api-slug: versapay
  description: Cancel an agreement.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/debit_agreements/{token}/cancel
  tags: Cancel,Agreements
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementstokencancel-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementstokencancel-post-openapi.md
- name: VersaPay Reject an Agreement
  x-api-slug: versapay
  description: Reject a *pending* agreement by supplying an agreement's *token* attribute
    and providing a *rejection_reason*.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/debit_agreements/{token}/reject
  tags: Reject,Agreements
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementstokenreject-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementstokenreject-post-openapi.md
- name: VersaPay Revoke an Agreement
  x-api-slug: versapay
  description: Revoke an *approved* agreement for your account by supplying an agreement's
    token attribute. The agreement's creator will no longer be able to debit your
    account using this agreement.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/debit_agreements/{token}/revoke
  tags: Revoke,Agreements
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementstokenrevoke-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apidebit-agreementstokenrevoke-post-openapi.md
- name: VersaPay Single Payment Hosted Checkout
  x-api-slug: versapay
  description: |-
    Clients, customers, or donors, for instance, can send your organization money directly from their bank account or credit card simply by clicking a link which displays a page with your account name allowing your customer to make a payment to you for the specified dollar amount:
    <br>
    `https://secure.versapay.com/send_money?api_token={your_api_token}&amount={dollar_amount_for_customer_to_pay}`
    <br>
    Funds will go to the fund destination passed in the to_fund parameter. By default, the funds will be deposited into your default bank account once the transaction clears from the other party.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////send_money
  tags: Single, Payment, Hosted, Checkout
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/send-money-get-openapi.md
- name: VersaPay Debit Agreement Hosted Checkout
  x-api-slug: versapay
  description: |-
    Clients, customers, or donors, for instance, can initiate a pre-authorized debit agreement by clicking a link on your website or in an email.
    <br>
    `https://secure.versapay.com/authorize?api_token={your_api_token}&message={explanation_of_what_this_is_for}`
    <br>
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////authorize
  tags: Debit, ,Agreements, Hosted, Checkout
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/authorize-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/authorize-get-openapi.md
- name: VersaPay Create and Update Customer
  x-api-slug: versapay
  description: |-
    Create a customer in ARC using the following attributes (at minimum by providing values for required attributes). If providing an identifier for an existing customer, its information is updated.<br><br>
    *Note: Any additional non-standard attribute will be stored with customer record and available for presentment rendering.*
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports/customer
  tags: Customer
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportscustomer-post-openapi.md
- name: VersaPay Create and Update Invoice
  x-api-slug: versapay
  description: |-
    Create and update invoices in ARC. If the invoice already exists when a request is processed, it will be updated.<br><br>
    The set of attributes to send in the request body may vary based on the account configuration. Please contact the implementation specialist for more information.<br><br>
    *Note:*
      * *Customer will be created/updated using the customer_&ast; attributes if necessary at time of invoice import.*
      * *Any additional non-standard attribute will be stored with invoice record and available for presentment rendering.*
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports/invoice
  tags: Invoice
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportsinvoice-post-openapi.md
- name: VersaPay Create a Payment
  x-api-slug: versapay
  description: "Create and update external payment records in ARC.<br><br>The set
    of attributes to send in the request body may vary based on the account configuration.
    Please contact the implementation specialist for more information.<br><br>\nThe
    request schema for posting a payment for a single invoice is slightly different
    than that for posting a payment for multiple invoices.\n\nFor instance, sample
    request for posting payment for a single invoice looks like:\n```\n{\n  \"identifier\":
    \"PMT0010-05\",\n  \"invoice_number\": \"INV1234-01\",\n  \"amount\": 10000,\n
    \ \"currency\": \"usd\",\n  \"date\": \"2018-01-10\",\n  \"customer_identifier\":
    \"C1234\",\n  \"customer_name\": \"Acme Inc.\",\n  \"notes\": \"Notes\",\n  \"ref1\":
    \"1234\",\n  \"ref2\": \"PO# 84767\"\n}\n```\n\n*Note: Customer will be created
    using the customer_&ast; attributes if it doesn\u2019t already exist at the time
    of payment import.*"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports/payment
  tags: CreatePayment
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportspayment-post-openapi.md
- name: VersaPay View In-Progress & Completed Batches
  x-api-slug: versapay
  description: View recent in-progress and completed import batches.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports
  tags: View, In-Progress, &, Completed, Batches
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimports-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimports-get-openapi.md
- name: VersaPay Import a CSV File
  x-api-slug: versapay
  description: "When uploading a CSV-formatted file it\u2019s helpful to use your
    language/framework tooling to simplify the [multipart/form-data](https://www.ietf.org/rfc/rfc2388.txt)
    file upload.\n### Size Limit\nThe file cannot exceed 25MB.\n### Layouts\nPlease
    contact support@versapay.com or reach out to your implementation specialist for
    standard inbound CSV file layouts."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports
  tags: ImportCSV, File
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimports-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimports-post-openapi.md
- name: VersaPay View In-Progress Batches
  x-api-slug: versapay
  description: View only recent in-progress import batches.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports/processing
  tags: View, In-Progress, Batches
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportsprocessing-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportsprocessing-get-openapi.md
- name: VersaPay View Completed Batches
  x-api-slug: versapay
  description: View only recent completed import batches.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports/completed
  tags: View, Completed, Batches
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportscompleted-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportscompleted-get-openapi.md
- name: VersaPay View Batch Details
  x-api-slug: versapay
  description: View batch details.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/imports/{id}
  tags: View, Batch, Details
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiimportsid-get-openapi.md
- name: VersaPay Payments made in ARC
  x-api-slug: versapay
  description: Payments made to your supplier account from your customers since watermark,
    limited to 100 payment amounts at a time.<br><br>A consumer should store the last
    `id` value of each response and include it as the watermark parameter for a subsequent
    calls.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/exports/payment_amounts
  tags: Payments, made, in, ARC
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiexportspayment-amounts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiexportspayment-amounts-get-openapi.md
- name: VersaPay Open and Closed Disputes
  x-api-slug: versapay
  description: Open and closed disputes since watermark, limited to 100 disputes at
    a time.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com////api/exports/disputes
  tags: OpenClosed, Disputes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiexportsdisputes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/apiexportsdisputes-get-openapi.md
- name: VersaPay
  x-api-slug: versapay
  description: VersaPay handles elements of both credit and debit card merchant payment
    processing in Canada. In offering a host of merchant account services and credit
    card POS terminals it allows for an efficient merchant payment service in all
    aspects- in person, on the go, online, and at the office. Founded in 2005 by Michael
    Gokturk, VersaPay is a Canadian owned and operated national financial transaction
    services provider partnered with Chase Paymentech. Versapay also offers electronic
    funds transfer through a system called Versapay EMT.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/1208-versapay-corporation.jpg
  humanURL: http://developers.versapay.com/index.html
  baseURL: https://secure.versapay.com//
  tags: VersaPay
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/versapay/master/_listings/versapay/openapi.md
x-common:
- type: x-base
  url: https://secure.versapay.com/api/
- type: x-blog
  url: https://www.versapay.com/blog/
- type: x-blog-rss
  url: http://www.versapay.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/versapay
- type: x-crunchbase
  url: https://crunchbase.com/organization/versapay
- type: x-github
  url: https://github.com/versapay
- type: x-partners
  url: https://www.versapay.com/partners/
- type: x-support
  url: https://www.versapay.com/support/
- type: x-twitter
  url: https://twitter.com/VersaPay
- type: x-website
  url: http://developers.versapay.com/index.html
- type: x-website
  url: https://www.versapay.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---