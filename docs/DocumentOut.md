# InvoicePDFs::DocumentOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **document_type** | **String** |  |  |
| **number** | **String** |  |  |
| **status** | **String** |  |  |
| **issue_date** | **Date** |  |  |
| **due_date** | **Date** |  | [optional] |
| **currency** | **String** |  |  |
| **locale** | **String** |  | [optional] |
| **business_profile_id** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **source_document_id** | **String** |  | [optional] |
| **reason** | **String** |  | [optional] |
| **data** | **Hash&lt;String, Object&gt;** |  |  |
| **totals** | [**InvoiceTotalsOut**](InvoiceTotalsOut.md) |  |  |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |
| **finalized_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentOut.new(
  id: null,
  document_type: null,
  number: null,
  status: null,
  issue_date: null,
  due_date: null,
  currency: null,
  locale: null,
  business_profile_id: null,
  customer_id: null,
  source_document_id: null,
  reason: null,
  data: null,
  totals: null,
  created_at: null,
  updated_at: null,
  finalized_at: null
)
```

