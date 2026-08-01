# InvoicePDFs::WebhookEndpointPatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **url** | **String** |  | [optional] |
| **description** | **String** |  | [optional] |
| **events** | **Array&lt;String&gt;** |  | [optional] |
| **is_active** | **Boolean** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::WebhookEndpointPatchRequest.new(
  url: null,
  description: null,
  events: null,
  is_active: null
)
```

