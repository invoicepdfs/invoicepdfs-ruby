# InvoicePDFs::DocumentRenderOptions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  | [optional][default to &#39;tpl_modern&#39;] |
| **page_size** | **String** |  | [optional][default to &#39;LETTER&#39;] |
| **expires_in** | **Integer** |  | [optional][default to 3600] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentRenderOptions.new(
  template_id: null,
  page_size: null,
  expires_in: null
)
```

