# InvoicePDFs::UsageOverage

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **enabled** | **Boolean** |  | [optional][default to false] |
| **available** | **Boolean** |  | [optional][default to false] |
| **renders** | **Integer** |  | [optional][default to 0] |
| **price_millicents** | **Integer** |  | [optional] |
| **estimated_cost_cents** | **Integer** |  | [optional][default to 0] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::UsageOverage.new(
  enabled: null,
  available: null,
  renders: null,
  price_millicents: null,
  estimated_cost_cents: null
)
```

