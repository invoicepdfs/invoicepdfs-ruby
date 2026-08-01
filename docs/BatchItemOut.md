# InvoicePDFs::BatchItemOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **external_id** | **String** |  | [optional] |
| **document_type** | **String** |  |  |
| **status** | **String** |  |  |
| **render_id** | **String** |  | [optional] |
| **error_message** | **String** |  | [optional] |
| **created_at** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BatchItemOut.new(
  id: null,
  external_id: null,
  document_type: null,
  status: null,
  render_id: null,
  error_message: null,
  created_at: null
)
```

