# InvoicePDFs::ComplianceViolationOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **rule** | **String** | The EN 16931 term or group. |  |
| **path** | **String** | Where in the document. |  |
| **message** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ComplianceViolationOut.new(
  rule: BT-130,
  path: lines[1].unit_code,
  message: A coded unit is required.
)
```

