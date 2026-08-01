# InvoicePDFs::TaxRatesListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;TaxRateOut&gt;**](TaxRateOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TaxRatesListResponse.new(
  data: null,
  pagination: null
)
```

