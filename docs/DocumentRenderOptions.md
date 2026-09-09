# InvoicePDFs::DocumentRenderOptions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  | [optional][default to &#39;tpl_modern&#39;] |
| **page_size** | **String** |  | [optional][default to &#39;LETTER&#39;] |
| **expires_in** | **Integer** |  | [optional][default to 3600] |
| **format** | **String** | &#x60;facturx_pdf&#x60; embeds the EN 16931 CII XML in a PDF/A-3, which is what a French or German counterparty means by Factur-X or ZUGFeRD. | [optional][default to &#39;pdf&#39;] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentRenderOptions.new(
  template_id: null,
  page_size: null,
  expires_in: null,
  format: pdf
)
```

