# InvoicePDFs::JobOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **type** | **String** |  |  |
| **status** | **String** |  |  |
| **progress** | [**JobProgressOut**](JobProgressOut.md) |  |  |
| **result** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **error** | **String** |  | [optional] |
| **created_at** | **String** |  |  |
| **started_at** | **String** |  | [optional] |
| **completed_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::JobOut.new(
  id: null,
  type: null,
  status: null,
  progress: null,
  result: null,
  error: null,
  created_at: null,
  started_at: null,
  completed_at: null
)
```

