# InvoicePDFs::TemplateCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **base_template_id** | **String** |  | [optional][default to &#39;tpl_modern&#39;] |
| **config** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TemplateCreateRequest.new(
  name: null,
  description: null,
  base_template_id: null,
  config: null
)
```

