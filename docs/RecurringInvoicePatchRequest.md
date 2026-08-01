# InvoicePDFs::RecurringInvoicePatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **frequency** | **String** |  | [optional] |
| **interval** | **Integer** |  | [optional] |
| **end_date** | **Date** |  | [optional] |
| **max_occurrences** | **Integer** |  | [optional] |
| **numbering_sequence_id** | **String** |  | [optional] |
| **auto_finalize** | **Boolean** |  | [optional] |
| **invoice_template** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::RecurringInvoicePatchRequest.new(
  frequency: null,
  interval: null,
  end_date: null,
  max_occurrences: null,
  numbering_sequence_id: null,
  auto_finalize: null,
  invoice_template: null
)
```

