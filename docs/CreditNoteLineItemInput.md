# InvoicePDFs::CreditNoteLineItemInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **quantity** | **String** |  |  |
| **unit_price** | **String** |  |  |
| **taxes** | [**Array&lt;InvoiceLineItemTaxInput&gt;**](InvoiceLineItemTaxInput.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CreditNoteLineItemInput.new(
  name: Web Development,
  description: null,
  quantity: 1,
  unit_price: 150.00,
  taxes: null
)
```

