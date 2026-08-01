# InvoicePDFs::DeliverySendRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **to** | **Array&lt;String&gt;** |  |  |
| **cc** | **Array&lt;String&gt;** |  | [optional] |
| **bcc** | **Array&lt;String&gt;** |  | [optional] |
| **subject** | **String** |  | [optional] |
| **message** | **String** |  | [optional] |
| **attach_pdf** | **Boolean** |  | [optional][default to true] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DeliverySendRequest.new(
  to: [&quot;client@example.com&quot;],
  cc: [],
  bcc: [],
  subject: null,
  message: null,
  attach_pdf: null
)
```

