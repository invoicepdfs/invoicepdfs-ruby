# InvoicePDFs::BusinessProfileCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **legal_name** | **String** |  |  |
| **display_name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **website** | **String** |  | [optional] |
| **tax_id** | **String** |  | [optional] |
| **address** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **default_currency** | **String** |  | [optional] |
| **default_locale** | **String** |  | [optional] |
| **default_timezone** | **String** |  | [optional] |
| **logo_file_id** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BusinessProfileCreate.new(
  legal_name: Acme Corp Inc.,
  display_name: null,
  email: null,
  phone: null,
  website: null,
  tax_id: null,
  address: null,
  default_currency: null,
  default_locale: null,
  default_timezone: null,
  logo_file_id: null
)
```

