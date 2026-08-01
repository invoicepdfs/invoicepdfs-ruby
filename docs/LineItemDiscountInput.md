# InvoicePDFs::LineItemDiscountInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  | [optional][default to &#39;percentage&#39;] |
| **value** | **String** |  |  |
| **reason** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::LineItemDiscountInput.new(
  type: null,
  value: 10,
  reason: null
)
```

