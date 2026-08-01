# InvoicePDFs::CustomTemplateOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **name** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **base_template_id** | **String** |  |  |
| **config** | **Hash&lt;String, Object&gt;** |  | [optional] |
| **status** | **String** |  |  |
| **is_default** | **Boolean** |  | [optional][default to false] |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |
| **published_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CustomTemplateOut.new(
  id: null,
  name: null,
  description: null,
  base_template_id: null,
  config: null,
  status: null,
  is_default: null,
  created_at: null,
  updated_at: null,
  published_at: null
)
```

