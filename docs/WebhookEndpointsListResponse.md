# InvoicePDFs::WebhookEndpointsListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;WebhookEndpointOut&gt;**](WebhookEndpointOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::WebhookEndpointsListResponse.new(
  data: null,
  pagination: null
)
```

