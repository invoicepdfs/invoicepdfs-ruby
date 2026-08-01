# InvoicePDFs::TemplateDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |
| **name** | **String** |  |  |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **engine** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TemplateDetail.new(
  template_id: null,
  name: null,
  document_type: null,
  engine: null
)
```

