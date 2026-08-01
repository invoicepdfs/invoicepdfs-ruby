# InvoicePDFs::WebhookDeliveryOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **endpoint_id** | **String** |  |  |
| **event_id** | **String** |  |  |
| **event_type** | **String** |  |  |
| **status** | **String** |  |  |
| **http_status** | **Integer** |  | [optional] |
| **attempts** | **Integer** |  |  |
| **error_message** | **String** |  | [optional] |
| **created_at** | **String** |  |  |
| **delivered_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::WebhookDeliveryOut.new(
  id: null,
  endpoint_id: null,
  event_id: null,
  event_type: null,
  status: null,
  http_status: null,
  attempts: null,
  error_message: null,
  created_at: null,
  delivered_at: null
)
```

