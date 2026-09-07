# InvoicePDFs::TaxCategory

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | UNCL5305 tax category code — S standard, Z zero-rated, E exempt, AE reverse charge, K intra-community, G export, O outside scope |  |
| **exemption_reason** | **String** |  | [optional] |
| **exemption_reason_code** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::TaxCategory.new(
  code: S,
  exemption_reason: null,
  exemption_reason_code: null
)
```

