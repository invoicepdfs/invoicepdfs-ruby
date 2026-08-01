# InvoicePDFs::RecurringInvoiceCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_profile_id** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **frequency** | **String** | daily, weekly, monthly, quarterly, or yearly |  |
| **interval** | **Integer** | Every N periods | [optional][default to 1] |
| **start_date** | **Date** | Date of the first invoice |  |
| **end_date** | **Date** |  | [optional] |
| **max_occurrences** | **Integer** |  | [optional] |
| **numbering_sequence_id** | **String** |  | [optional] |
| **auto_finalize** | **Boolean** | Automatically finalize generated invoices | [optional][default to false] |
| **invoice_template** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::RecurringInvoiceCreateRequest.new(
  business_profile_id: null,
  customer_id: null,
  frequency: null,
  interval: null,
  start_date: null,
  end_date: null,
  max_occurrences: null,
  numbering_sequence_id: null,
  auto_finalize: null,
  invoice_template: null
)
```

