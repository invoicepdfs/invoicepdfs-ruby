# InvoicePDFs::TaxRateCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **rate** | **String** |  |  |
| **inclusive** | **Boolean** |  | [optional][default to false] |
| **jurisdiction** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TaxRateCreateRequest.new(
  name: California sales tax,
  rate: 8.375,
  inclusive: null,
  jurisdiction: null
)
```

