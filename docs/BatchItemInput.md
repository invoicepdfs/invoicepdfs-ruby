# InvoicePDFs::BatchItemInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **external_id** | **String** |  | [optional] |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **data** | **Hash&lt;String, Object&gt;** | Document data payload |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BatchItemInput.new(
  external_id: null,
  document_type: null,
  data: null
)
```

