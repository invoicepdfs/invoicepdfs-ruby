# InvoicePDFs::ComplianceCheckOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile** | **String** |  |  |
| **ruleset_version** | **String** | The version these rules came from. Worth recording alongside any document you file — rulesets revise, and &#39;which rules did this pass?&#39; is what an audit asks years later. |  |
| **valid** | **Boolean** |  |  |
| **violations** | [**Array&lt;ComplianceViolationOut&gt;**](ComplianceViolationOut.md) | Every violation found, not the first — fixing one field per round trip is the experience this avoids. | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ComplianceCheckOut.new(
  profile: peppol_bis_billing_3,
  ruleset_version: PEPPOL-UBL-3.15.0,
  valid: null,
  violations: null
)
```

