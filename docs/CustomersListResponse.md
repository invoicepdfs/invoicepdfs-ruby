# InvoicePDFs::CustomersListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;CustomerOut&gt;**](CustomerOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CustomersListResponse.new(
  data: null,
  pagination: null
)
```

