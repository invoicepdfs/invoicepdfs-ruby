# InvoicePDFs::BrandingProfileOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **name** | **String** |  |  |
| **is_default** | **Boolean** |  |  |
| **logo_file_id** | **String** |  | [optional] |
| **primary_color** | **String** |  |  |
| **accent_color** | **String** |  |  |
| **font_family** | **String** |  | [optional] |
| **header_text** | **String** |  | [optional] |
| **footer_text** | **String** |  |  |
| **hide_invoicepdfs_branding** | **Boolean** |  |  |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BrandingProfileOut.new(
  id: null,
  name: null,
  is_default: null,
  logo_file_id: null,
  primary_color: null,
  accent_color: null,
  font_family: null,
  header_text: null,
  footer_text: null,
  hide_invoicepdfs_branding: null,
  created_at: null,
  updated_at: null
)
```

