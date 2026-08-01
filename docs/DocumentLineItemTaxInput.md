# InvoicePDFs::DocumentLineItemTaxInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **rate** | **String** |  |  |
| **inclusive** | **Boolean** |  | [optional][default to false] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentLineItemTaxInput.new(
  name: Sales Tax,
  rate: 8.875,
  inclusive: null
)
```

