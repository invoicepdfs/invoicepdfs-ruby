# InvoicePDFs::BatchOutputOptions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **format** | **String** |  | [optional][default to &#39;pdf&#39;] |
| **combine** | **Boolean** |  | [optional][default to false] |
| **archive_format** | **String** |  | [optional][default to &#39;zip&#39;] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BatchOutputOptions.new(
  format: null,
  combine: null,
  archive_format: null
)
```

