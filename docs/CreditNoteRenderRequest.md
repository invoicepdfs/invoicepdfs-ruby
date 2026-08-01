# InvoicePDFs::CreditNoteRenderRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  | [optional][default to &#39;tpl_modern&#39;] |
| **page_size** | **String** |  | [optional][default to &#39;LETTER&#39;] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CreditNoteRenderRequest.new(
  template_id: null,
  page_size: null
)
```

