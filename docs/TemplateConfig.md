# InvoicePDFs::TemplateConfig

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **primary_color** | **String** |  | [optional] |
| **accent_color** | **String** |  | [optional] |
| **font_family** | **String** |  | [optional] |
| **header_text** | **String** |  | [optional] |
| **footer_text** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TemplateConfig.new(
  primary_color: null,
  accent_color: null,
  font_family: null,
  header_text: null,
  footer_text: null
)
```

