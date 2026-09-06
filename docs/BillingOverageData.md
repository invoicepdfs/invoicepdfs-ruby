# InvoicePDFs::BillingOverageData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **overage_enabled** | **Boolean** |  |  |
| **overage_available** | **Boolean** |  |  |
| **overage_price_millicents** | **Integer** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BillingOverageData.new(
  overage_enabled: null,
  overage_available: null,
  overage_price_millicents: null
)
```

