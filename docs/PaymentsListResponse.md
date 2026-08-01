# InvoicePDFs::PaymentsListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;PaymentOut&gt;**](PaymentOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::PaymentsListResponse.new(
  data: null,
  pagination: null
)
```

