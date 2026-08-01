# InvoicePDFs::PaymentPatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **String** |  | [optional] |
| **paid_at** | **Time** |  | [optional] |
| **method** | **String** |  | [optional] |
| **reference** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::PaymentPatchRequest.new(
  amount: null,
  paid_at: null,
  method: null,
  reference: null,
  notes: null
)
```

