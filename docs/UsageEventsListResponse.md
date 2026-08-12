# InvoicePDFs::UsageEventsListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;UsageEventOut&gt;**](UsageEventOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::UsageEventsListResponse.new(
  data: null,
  pagination: null
)
```

