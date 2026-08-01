# InvoicePDFs::DocumentPaymentInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bank_account** | [**InvoiceBankAccountInput**](InvoiceBankAccountInput.md) |  | [optional] |
| **payment_url** | **String** |  | [optional] |
| **accepted_methods** | **Array&lt;String&gt;** |  | [optional] |
| **instructions** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentPaymentInput.new(
  bank_account: null,
  payment_url: null,
  accepted_methods: [&quot;bank_transfer&quot;,&quot;credit_card&quot;],
  instructions: null
)
```

