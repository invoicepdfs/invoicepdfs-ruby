# InvoicePDFs::BillingSubscriptionData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_id** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **plan_id** | **String** |  |  |
| **plan_name** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BillingSubscriptionData.new(
  subscription_id: null,
  status: null,
  plan_id: null,
  plan_name: null
)
```

