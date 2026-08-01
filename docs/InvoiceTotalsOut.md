# InvoicePDFs::InvoiceTotalsOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subtotal** | [**MoneyOut**](MoneyOut.md) |  |  |
| **discount_total** | [**MoneyOut**](MoneyOut.md) |  |  |
| **tax_total** | [**MoneyOut**](MoneyOut.md) |  |  |
| **shipping_total** | [**MoneyOut**](MoneyOut.md) |  |  |
| **total** | [**MoneyOut**](MoneyOut.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceTotalsOut.new(
  subtotal: null,
  discount_total: null,
  tax_total: null,
  shipping_total: null,
  total: null
)
```

