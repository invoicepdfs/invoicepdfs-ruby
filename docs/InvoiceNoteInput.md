# InvoicePDFs::InvoiceNoteInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **content** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceNoteInput.new(
  type: note,
  content: Thank you for your business!
)
```

