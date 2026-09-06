# InvoicePDFs::UsageLimitsData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **renders** | [**UsageRenderLimits**](UsageRenderLimits.md) |  |  |
| **rate_limit** | [**UsageRateLimit**](UsageRateLimit.md) |  |  |
| **api_log_retention** | **Integer** |  | [optional][default to 0] |
| **overage** | [**UsageOverage**](UsageOverage.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::UsageLimitsData.new(
  renders: null,
  rate_limit: null,
  api_log_retention: null,
  overage: null
)
```

