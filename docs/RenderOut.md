# InvoicePDFs::RenderOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **status** | **String** |  |  |
| **document_type** | **String** |  |  |
| **template_id** | **String** |  |  |
| **template_version** | **Integer** |  | [optional] |
| **format** | **String** |  |  |
| **download_url** | **String** |  |  |
| **expires_at** | **String** |  |  |
| **calculation** | [**CalculationBreakdown**](CalculationBreakdown.md) |  |  |
| **created_at** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::RenderOut.new(
  id: null,
  status: null,
  document_type: null,
  template_id: null,
  template_version: null,
  format: null,
  download_url: null,
  expires_at: null,
  calculation: null,
  created_at: null
)
```

