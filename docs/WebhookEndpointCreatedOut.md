# InvoicePDFs::WebhookEndpointCreatedOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **url** | **String** |  |  |
| **description** | **String** |  | [optional] |
| **events** | **Array&lt;String&gt;** |  |  |
| **is_active** | **Boolean** |  |  |
| **created_at** | **String** |  |  |
| **updated_at** | **String** |  |  |
| **secret** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::WebhookEndpointCreatedOut.new(
  id: null,
  url: null,
  description: null,
  events: null,
  is_active: null,
  created_at: null,
  updated_at: null,
  secret: null
)
```

