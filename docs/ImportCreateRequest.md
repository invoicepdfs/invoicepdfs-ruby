# InvoicePDFs::ImportCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **source_format** | **String** |  |  |
| **data** | **Array&lt;Hash&lt;String, Object&gt;&gt;** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ImportCreateRequest.new(
  source_format: csv,
  data: null
)
```

