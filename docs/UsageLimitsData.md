# InvoicePDFs::UsageLimitsData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **renders** | [**UsageRenderLimits**](UsageRenderLimits.md) |  |  |
| **rate_limit** | [**UsageRateLimit**](UsageRateLimit.md) |  |  |
| **overage** | [**UsageOverage**](UsageOverage.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::UsageLimitsData.new(
  renders: null,
  rate_limit: null,
  overage: null
)
```

