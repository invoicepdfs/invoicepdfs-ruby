# InvoicePDFs::DocumentsListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;DocumentOut&gt;**](DocumentOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentsListResponse.new(
  data: null,
  pagination: null
)
```

