# InvoicePDFs::WorkspaceMemberCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **email** | **String** |  |  |
| **role** | **String** |  | [optional][default to &#39;member&#39;] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::WorkspaceMemberCreateRequest.new(
  email: teammate@acme.com,
  role: null
)
```

