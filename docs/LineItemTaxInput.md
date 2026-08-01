# InvoicePDFs::LineItemTaxInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tax_rate_id** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **rate** | **String** |  | [optional] |
| **inclusive** | **Boolean** |  | [optional][default to false] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::LineItemTaxInput.new(
  tax_rate_id: null,
  name: null,
  rate: null,
  inclusive: null
)
```

