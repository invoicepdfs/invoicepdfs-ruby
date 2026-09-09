# InvoicePDFs::CustomerPatch

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **contact_name** | **String** |  | [optional] |
| **email** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **tax_id** | **String** |  | [optional] |
| **billing_address** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **shipping_address** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **electronic_address** | [**ElectronicAddress**](ElectronicAddress.md) |  | [optional] |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CustomerPatch.new(
  name: null,
  contact_name: null,
  email: null,
  phone: null,
  tax_id: null,
  billing_address: null,
  shipping_address: null,
  electronic_address: null,
  metadata: null
)
```

