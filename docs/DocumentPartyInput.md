# InvoicePDFs::DocumentPartyInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **legal_name** | **String** |  | [optional] |
| **contact_name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **website** | **String** |  | [optional] |
| **tax_id** | **String** |  | [optional] |
| **registration_number** | **String** |  | [optional] |
| **address** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **bank_account** | [**InvoiceBankAccountInput**](InvoiceBankAccountInput.md) |  | [optional] |
| **electronic_address** | [**ElectronicAddress**](ElectronicAddress.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentPartyInput.new(
  name: Acme Corp,
  legal_name: null,
  contact_name: null,
  email: null,
  phone: null,
  website: null,
  tax_id: null,
  registration_number: null,
  address: null,
  bank_account: null,
  electronic_address: null
)
```

