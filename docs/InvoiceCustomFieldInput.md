# InvoicePDFs::InvoiceCustomFieldInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **label** | **String** |  |  |
| **value** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceCustomFieldInput.new(
  label: PO Number,
  value: PO-2026-001
)
```

