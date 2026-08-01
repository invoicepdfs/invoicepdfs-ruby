# InvoicePDFs::CreditNoteCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **credit_note_number** | **String** |  |  |
| **issue_date** | **Date** |  |  |
| **reason** | **String** |  | [optional] |
| **line_items** | [**Array&lt;CreditNoteLineItemInput&gt;**](CreditNoteLineItemInput.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CreditNoteCreateRequest.new(
  invoice_id: inv_01ABC,
  credit_note_number: CN-2026-001,
  issue_date: Mon Jul 20 00:00:00 UTC 2026,
  reason: null,
  line_items: null
)
```

