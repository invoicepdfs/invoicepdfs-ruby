# InvoicePDFs::InvoiceTotalsOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **gross_subtotal** | [**MoneyOut**](MoneyOut.md) |  | [optional] |
| **subtotal** | [**MoneyOut**](MoneyOut.md) |  |  |
| **discount_total** | [**MoneyOut**](MoneyOut.md) |  |  |
| **document_discount_total** | [**MoneyOut**](MoneyOut.md) |  | [optional] |
| **tax_total** | [**MoneyOut**](MoneyOut.md) |  |  |
| **shipping_total** | [**MoneyOut**](MoneyOut.md) |  |  |
| **total** | [**MoneyOut**](MoneyOut.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceTotalsOut.new(
  gross_subtotal: null,
  subtotal: null,
  discount_total: null,
  document_discount_total: null,
  tax_total: null,
  shipping_total: null,
  total: null
)
```

