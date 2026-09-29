# InvoicePDFs::ReadyResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  |  |
| **dependencies** | **Hash&lt;String, String&gt;** |  |  |
| **workers** | **Hash&lt;String, String&gt;** |  | [optional] |
| **degraded** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ReadyResponse.new(
  status: null,
  dependencies: null,
  workers: null,
  degraded: null
)
```

