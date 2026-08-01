# InvoicePDFs::PaymentCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **String** |  |  |
| **paid_at** | **Time** |  |  |
| **method** | **String** |  | [optional] |
| **reference** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::PaymentCreateRequest.new(
  amount: 53.10,
  paid_at: 2026-07-17T18:30Z,
  method: null,
  reference: null,
  notes: null
)
```

