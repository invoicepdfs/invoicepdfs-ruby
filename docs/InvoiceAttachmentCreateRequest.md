# InvoicePDFs::InvoiceAttachmentCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file_id** | **String** |  |  |
| **label** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceAttachmentCreateRequest.new(
  file_id: fil_01ABC,
  label: null
)
```

