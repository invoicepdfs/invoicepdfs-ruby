# InvoicePDFs::CreditNotesListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;CreditNoteOut&gt;**](CreditNoteOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CreditNotesListResponse.new(
  data: null,
  pagination: null
)
```

