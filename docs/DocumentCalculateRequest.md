# InvoicePDFs::DocumentCalculateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **data** | [**DocumentInvoiceDataInput**](DocumentInvoiceDataInput.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentCalculateRequest.new(
  document_type: null,
  data: null
)
```

