# InvoicePDFs::RecurringInvoiceOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **status** | **String** |  |  |
| **business_profile_id** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **frequency** | **String** |  |  |
| **interval** | **Integer** |  |  |
| **next_occurrence_date** | **Date** |  |  |
| **end_date** | **Date** |  |  |
| **occurrences_created** | **Integer** |  |  |
| **max_occurrences** | **Integer** |  |  |
| **numbering_sequence_id** | **String** |  |  |
| **auto_finalize** | **Boolean** |  |  |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::RecurringInvoiceOut.new(
  id: null,
  status: null,
  business_profile_id: null,
  customer_id: null,
  frequency: null,
  interval: null,
  next_occurrence_date: null,
  end_date: null,
  occurrences_created: null,
  max_occurrences: null,
  numbering_sequence_id: null,
  auto_finalize: null,
  created_at: null,
  updated_at: null
)
```

