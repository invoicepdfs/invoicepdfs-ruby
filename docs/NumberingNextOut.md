# InvoicePDFs::NumberingNextOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **number** | **String** |  |  |
| **sequence_id** | **String** |  |  |
| **next_number** | **Integer** | The counter after this allocation |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::NumberingNextOut.new(
  number: AMI-INV-2026-0013,
  sequence_id: null,
  next_number: null
)
```

