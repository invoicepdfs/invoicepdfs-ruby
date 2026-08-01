# InvoicePDFs::InvoicesListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;InvoiceOut&gt;**](InvoiceOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoicesListResponse.new(
  data: null,
  pagination: null
)
```

