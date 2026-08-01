# InvoicePDFs::CursorPagination

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **has_more** | **Boolean** |  | [optional][default to false] |
| **next_cursor** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CursorPagination.new(
  has_more: null,
  next_cursor: null
)
```

