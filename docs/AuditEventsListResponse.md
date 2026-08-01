# InvoicePDFs::AuditEventsListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;AuditEventOut&gt;**](AuditEventOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::AuditEventsListResponse.new(
  data: null,
  pagination: null
)
```

