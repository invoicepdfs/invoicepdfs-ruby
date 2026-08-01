# InvoicePDFs::ApiKeyListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;ApiKeyListItem&gt;**](ApiKeyListItem.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ApiKeyListResponse.new(
  data: null,
  pagination: null
)
```

