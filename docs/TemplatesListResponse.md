# InvoicePDFs::TemplatesListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;TemplateSummary&gt;**](TemplateSummary.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TemplatesListResponse.new(
  data: null,
  pagination: null
)
```

