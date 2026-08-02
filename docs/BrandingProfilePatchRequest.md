# InvoicePDFs::BrandingProfilePatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **primary_color** | **String** |  | [optional] |
| **accent_color** | **String** |  | [optional] |
| **font_family** | **String** |  | [optional] |
| **header_text** | **String** |  | [optional] |
| **footer_text** | **String** |  | [optional] |
| **hide_invoicepdfs_branding** | **Boolean** |  | [optional] |
| **is_default** | **Boolean** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BrandingProfilePatchRequest.new(
  name: null,
  primary_color: null,
  accent_color: null,
  font_family: null,
  header_text: null,
  footer_text: null,
  hide_invoicepdfs_branding: null,
  is_default: null
)
```

