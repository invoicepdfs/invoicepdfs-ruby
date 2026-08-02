# InvoicePDFs::BillingSubscriptionData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **subscription_id** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |
| **plan_id** | **String** |  |  |
| **plan_name** | **String** |  |  |
| **stripe_configured** | **Boolean** |  | [optional][default to false] |
| **has_billing_account** | **Boolean** |  | [optional][default to false] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BillingSubscriptionData.new(
  subscription_id: null,
  status: null,
  plan_id: null,
  plan_name: null,
  stripe_configured: null,
  has_billing_account: null
)
```

