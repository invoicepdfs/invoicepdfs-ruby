# InvoicePDFs::DocumentLineItemInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **quantity** | **String** |  |  |
| **unit_price** | **String** | Decimal string in major units |  |
| **unit** | **String** |  | [optional] |
| **sku** | **String** |  | [optional] |
| **discount** | [**DocumentDiscountInput**](DocumentDiscountInput.md) |  | [optional] |
| **taxes** | [**Array&lt;DocumentLineItemTaxInput&gt;**](DocumentLineItemTaxInput.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentLineItemInput.new(
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

