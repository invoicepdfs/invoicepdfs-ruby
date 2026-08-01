# InvoicePDFs::WebhookDeliveriesListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;WebhookDeliveryOut&gt;**](WebhookDeliveryOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::WebhookDeliveriesListResponse.new(
  data: null,
  pagination: null
)
```

