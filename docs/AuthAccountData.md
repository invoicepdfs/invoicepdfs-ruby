# InvoicePDFs::AuthAccountData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **account_id** | **String** |  |  |
| **name** | **String** |  |  |
| **email** | **String** |  | [optional] |
| **plan_id** | **String** |  |  |
| **plan_name** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::AuthAccountData.new(
  account_id: null,
  name: null,
  email: null,
  plan_id: null,
  plan_name: null
)
```

