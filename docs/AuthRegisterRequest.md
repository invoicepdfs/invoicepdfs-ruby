# InvoicePDFs::AuthRegisterRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id_token** | **String** | Firebase ID token from client-side auth |  |
| **name** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::AuthRegisterRequest.new(
  id_token: null,
  name: null
)
```

