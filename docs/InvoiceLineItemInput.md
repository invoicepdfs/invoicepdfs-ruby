# InvoicePDFs::InvoiceLineItemInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **quantity** | **String** | Decimal string |  |
| **unit_price** | **String** | Decimal string in major units |  |
| **unit** | **String** |  | [optional] |
| **sku** | **String** |  | [optional] |
| **discount** | [**InvoiceDiscountInput**](InvoiceDiscountInput.md) |  | [optional] |
| **taxes** | [**Array&lt;InvoiceLineItemTaxInput&gt;**](InvoiceLineItemTaxInput.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceLineItemInput.new(
  name: Web Development,
  description: null,
  quantity: 2,
  unit_price: 150.00,
  unit: null,
  sku: null,
  discount: null,
  taxes: null
)
```

