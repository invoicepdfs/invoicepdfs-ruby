# InvoicePDFs::InvoiceShippingInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** |  | [optional][default to &#39;Shipping&#39;] |
| **amount** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceShippingInput.new(
  description: null,
  amount: 9.99
)
```

