# InvoicePDFs::DocumentShippingInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** |  | [optional][default to &#39;Shipping&#39;] |
| **amount** | **String** |  |  |
| **taxable** | **Boolean** |  | [optional][default to false] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentShippingInput.new(
  description: null,
  amount: 9.99,
  taxable: null
)
```

