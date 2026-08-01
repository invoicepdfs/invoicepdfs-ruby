# InvoicePDFs::AppSchemasV1DocumentRenderRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **data** | [**DocumentInvoiceDataInput**](DocumentInvoiceDataInput.md) |  |  |
| **template** | [**DocumentTemplateRef**](DocumentTemplateRef.md) |  |  |
| **output** | [**DocumentOutputOptions**](DocumentOutputOptions.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::AppSchemasV1DocumentRenderRequest.new(
  document_type: null,
  data: null,
  template: null,
  output: null
)
```

