# InvoicePDFs::ImportOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **source_format** | **String** |  |  |
| **status** | **String** |  |  |
| **total_rows** | **Integer** |  |  |
| **imported_rows** | **Integer** |  |  |
| **failed_rows** | **Integer** |  |  |
| **errors** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  | [optional] |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |
| **completed_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ImportOut.new(
  id: null,
  source_format: null,
  status: null,
  total_rows: null,
  imported_rows: null,
  failed_rows: null,
  errors: null,
  created_at: null,
  updated_at: null,
  completed_at: null
)
```

