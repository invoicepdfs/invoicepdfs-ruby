# InvoicePDFs::InvoiceTermInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **content** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceTermInput.new(
  type: term,
  content: Net 30 — payment due within 30 days of invoice date.
)
```

