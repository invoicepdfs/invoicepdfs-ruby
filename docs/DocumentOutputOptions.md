# InvoicePDFs::DocumentOutputOptions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **format** | **String** |  | [optional][default to &#39;pdf&#39;] |
| **delivery** | **String** |  | [optional][default to &#39;url&#39;] |
| **expires_in** | **Integer** |  | [optional][default to 3600] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentOutputOptions.new(
  format: null,
  delivery: null,
  expires_in: null
)
```

