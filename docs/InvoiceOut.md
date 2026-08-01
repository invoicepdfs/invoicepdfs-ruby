# InvoicePDFs::InvoiceOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **status** | **String** |  |  |
| **invoice_number** | **String** |  |  |
| **document_type** | **String** |  |  |
| **issue_date** | **Date** |  |  |
| **due_date** | **Date** |  | [optional] |
| **currency** | **String** |  |  |
| **locale** | **String** |  | [optional] |
| **business_profile_id** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **invoice** | **Hash&lt;String, Object&gt;** |  |  |
| **totals** | [**InvoiceTotalsOut**](InvoiceTotalsOut.md) |  |  |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |
| **finalized_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceOut.new(
  id: null,
  status: null,
  invoice_number: null,
  document_type: null,
  issue_date: null,
  due_date: null,
  currency: null,
  locale: null,
  business_profile_id: null,
  customer_id: null,
  invoice: null,
  totals: null,
  created_at: null,
  updated_at: null,
  finalized_at: null
)
```

