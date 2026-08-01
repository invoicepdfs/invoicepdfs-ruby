# InvoicePDFs::DocumentValidateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **data** | [**DocumentInvoiceDataInput**](DocumentInvoiceDataInput.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentValidateRequest.new(
  document_type: null,
  data: null
)
```

