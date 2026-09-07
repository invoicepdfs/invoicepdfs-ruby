# InvoicePDFs::TaxRatePatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **rate** | **String** |  | [optional] |
| **inclusive** | **Boolean** |  | [optional] |
| **jurisdiction** | **String** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |
| **category** | [**TaxCategory**](TaxCategory.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TaxRatePatchRequest.new(
  name: null,
  rate: null,
  inclusive: null,
  jurisdiction: null,
  is_active: null,
  category: null
)
```

