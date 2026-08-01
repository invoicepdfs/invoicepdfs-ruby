# InvoicePDFs::AuthResetPasswordRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **oob_code** | **String** | Code from the password reset email |  |
| **new_password** | **String** | New password |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::AuthResetPasswordRequest.new(
  oob_code: null,
  new_password: null
)
```

