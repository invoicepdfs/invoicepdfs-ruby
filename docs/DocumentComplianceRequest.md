# InvoicePDFs::DocumentComplianceRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **data** | [**DocumentInvoiceDataInput**](DocumentInvoiceDataInput.md) |  |  |
| **profile** | **String** | Which ruleset to hold the document to. Rulesets differ: a document valid under one can be rejected by another, so there is no default. |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentComplianceRequest.new(
  document_type: null,
  data: null,
  profile: peppol_bis_billing_3
)
```

