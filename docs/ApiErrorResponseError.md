# InvoicePDFs::ApiErrorResponseError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **Integer** | HTTP status, mirroring the response status line. |  |
| **code** | **String** |  |  |
| **message** | **String** |  |  |
| **request_id** | **String** | Trace id for this request; also returned as X-Trace-Id. | [optional] |
| **details** | **Object** | Error-specific context. Validation failures carry &#x60;fields&#x60;. | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ApiErrorResponseError.new(
  status: 422,
  code: unprocessable_entity,
  message: Request validation failed,
  request_id: null,
  details: null
)
```

