# InvoicePDFs::DocumentTypeOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **name** | **String** |  |  |
| **number_prefix** | **String** |  |  |
| **payable** | **Boolean** |  |  |
| **requires_source_document** | **Boolean** |  |  |
| **supports_reason** | **Boolean** |  |  |
| **line_item_type** | **String** |  |  |
| **actions** | **Array&lt;String&gt;** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentTypeOut.new(
  id: null,
  name: null,
  number_prefix: null,
  payable: null,
  requires_source_document: null,
  supports_reason: null,
  line_item_type: null,
  actions: null
)
```

