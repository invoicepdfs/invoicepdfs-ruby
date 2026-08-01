# InvoicePDFs::DocumentCustomFieldInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **label** | **String** |  |  |
| **value** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentCustomFieldInput.new(
  label: PO Number,
  value: PO-2026-001
)
```

