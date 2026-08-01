# InvoicePDFs::BatchOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **status** | **String** |  |  |
| **operation** | **String** |  |  |
| **template_id** | **String** |  |  |
| **total_items** | **Integer** |  |  |
| **completed_items** | **Integer** |  |  |
| **failed_items** | **Integer** |  |  |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |
| **completed_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BatchOut.new(
  id: null,
  status: null,
  operation: null,
  template_id: null,
  total_items: null,
  completed_items: null,
  failed_items: null,
  created_at: null,
  updated_at: null,
  completed_at: null
)
```

