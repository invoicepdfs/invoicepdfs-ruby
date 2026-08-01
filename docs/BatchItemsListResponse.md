# InvoicePDFs::BatchItemsListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;BatchItemOut&gt;**](BatchItemOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BatchItemsListResponse.new(
  data: null,
  pagination: null
)
```

