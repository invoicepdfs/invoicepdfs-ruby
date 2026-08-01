# InvoicePDFs::StandardLineItemInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **quantity** | **String** | Decimal string |  |
| **unit_price** | **String** | Decimal string, major units | [optional][default to &#39;0.00&#39;] |
| **unit** | **String** |  | [optional] |
| **sku** | **String** |  | [optional] |
| **discount** | [**LineItemDiscountInput**](LineItemDiscountInput.md) |  | [optional] |
| **taxes** | [**Array&lt;LineItemTaxInput&gt;**](LineItemTaxInput.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::StandardLineItemInput.new(
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

