# InvoicePDFs::InvoiceBankAccountInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **bank_name** | **String** |  | [optional] |
| **account_name** | **String** |  | [optional] |
| **account_number** | **String** |  | [optional] |
| **routing_number** | **String** |  | [optional] |
| **swift** | **String** |  | [optional] |
| **iban** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoiceBankAccountInput.new(
  bank_name: null,
  account_name: null,
  account_number: null,
  routing_number: null,
  swift: null,
  iban: null
)
```

