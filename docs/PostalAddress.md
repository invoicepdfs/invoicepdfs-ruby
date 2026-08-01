# InvoicePDFs::PostalAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **line1** | **String** |  |  |
| **line2** | **String** |  | [optional] |
| **city** | **String** |  | [optional] |
| **state** | **String** |  | [optional] |
| **postal_code** | **String** |  | [optional] |
| **country** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::PostalAddress.new(
  line1: 1 Main St,
  line2: null,
  city: null,
  state: null,
  postal_code: null,
  country: null
)
```

