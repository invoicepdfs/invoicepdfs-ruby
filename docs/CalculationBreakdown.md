# InvoicePDFs::CalculationBreakdown

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subtotal** | [**Money**](Money.md) |  |  |
| **discount_total** | [**Money**](Money.md) |  |  |
| **document_discount_total** | [**Money**](Money.md) |  | [optional] |
| **tax_total** | [**Money**](Money.md) |  |  |
| **shipping_total** | [**Money**](Money.md) |  |  |
| **total** | [**Money**](Money.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CalculationBreakdown.new(
  subtotal: null,
  discount_total: null,
  document_discount_total: null,
  tax_total: null,
  shipping_total: null,
  total: null
)
```

