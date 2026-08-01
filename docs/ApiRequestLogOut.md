# InvoicePDFs::ApiRequestLogOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **method** | **String** |  |  |
| **path** | **String** |  |  |
| **query** | **String** |  | [optional] |
| **status_code** | **Integer** |  |  |
| **duration_ms** | **Integer** |  | [optional] |
| **request_body** | **String** |  | [optional] |
| **response_body** | **String** |  | [optional] |
| **created_at** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ApiRequestLogOut.new(
  id: null,
  method: null,
  path: null,
  query: null,
  status_code: null,
  duration_ms: null,
  request_body: null,
  response_body: null,
  created_at: null
)
```

