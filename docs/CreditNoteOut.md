# InvoicePDFs::CreditNoteOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **invoice_id** | **String** |  |  |
| **credit_note_number** | **String** |  |  |
| **status** | **String** |  |  |
| **reason** | **String** |  | [optional] |
| **currency** | **String** |  |  |
| **totals** | [**InvoiceTotalsOut**](InvoiceTotalsOut.md) |  |  |
| **issue_date** | **Date** |  |  |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |
| **finalized_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CreditNoteOut.new(
  id: null,
  invoice_id: null,
  credit_note_number: null,
  status: null,
  reason: null,
  currency: null,
  totals: null,
  issue_date: null,
  created_at: null,
  updated_at: null,
  finalized_at: null
)
```

