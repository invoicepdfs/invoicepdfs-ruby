# InvoicePDFs::WebhookEndpointCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **events** | **Array&lt;String&gt;** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::WebhookEndpointCreateRequest.new(
  url: https://example.com/webhooks,
  description: null,
  events: [&quot;invoice.created&quot;,&quot;invoice.paid&quot;]
)
```

