# InvoicePDFs::ElectronicAddress

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **value** | **String** |  |  |
| **scheme_id** | **String** | EAS code list identifier — 0088 is GLN, 9930 a German VAT number. |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ElectronicAddress.new(
  value: 9482348239,
  scheme_id: 0088
)
```

