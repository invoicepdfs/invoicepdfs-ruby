# InvoicePDFs::PaymentOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **invoice_id** | **String** |  |  |
| **amount** | [**MoneyOut**](MoneyOut.md) |  |  |
| **paid_at** | **String** |  |  |
| **method** | **String** |  | [optional] |
| **reference** | **String** |  | [optional] |
| **notes** | **String** |  | [optional] |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::PaymentOut.new(
  id: null,
  invoice_id: null,
  amount: null,
  paid_at: null,
  method: null,
  reference: null,
  notes: null,
  created_at: null,
  updated_at: null
)
```

