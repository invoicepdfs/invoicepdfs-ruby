# InvoicePDFs::BillingPlan

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **name** | **String** |  |  |
| **price_id** | **String** |  |  |
| **price_id_annual** | **String** |  | [optional] |
| **price_cents** | **Integer** |  | [optional] |
| **price_cents_annual** | **Integer** |  | [optional] |
| **monthly_render_quota** | **Integer** |  |  |
| **allow_branding_removal** | **Boolean** |  | [optional][default to false] |
| **overage_price_millicents** | **Integer** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BillingPlan.new(
  id: null,
  name: null,
  price_id: null,
  price_id_annual: null,
  price_cents: null,
  price_cents_annual: null,
  monthly_render_quota: null,
  allow_branding_removal: null,
  overage_price_millicents: null
)
```

