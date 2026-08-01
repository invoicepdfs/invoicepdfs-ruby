# InvoicePDFs::BrandingUpdateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **primary_color** | **String** |  | [optional] |
| **accent_color** | **String** |  | [optional] |
| **font_family** | **String** |  | [optional] |
| **footer_text** | **String** |  | [optional] |
| **hide_invoicepdfs_branding** | **Boolean** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BrandingUpdateRequest.new(
  primary_color: null,
  accent_color: null,
  font_family: null,
  footer_text: null,
  hide_invoicepdfs_branding: null
)
```

