# InvoicePDFs::DeliveriesListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;DeliveryOut&gt;**](DeliveryOut.md) |  |  |
| **pagination** | [**CursorPagination**](CursorPagination.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DeliveriesListResponse.new(
  data: null,
  pagination: null
)
```

