# InvoicePDFs::CustomerCreate

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **email** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **tax_id** | **String** |  | [optional] |
| **billing_address** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **shipping_address** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **metadata** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CustomerCreate.new(
  name: Jane Smith,
  email: null,
  phone: null,
  tax_id: null,
  billing_address: null,
  shipping_address: null,
  metadata: null
)
```

