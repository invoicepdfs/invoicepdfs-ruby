# InvoicePDFs::ComplianceCheckOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile** | **String** |  |  |
| **ruleset_version** | **String** | The version these rules came from. Worth recording alongside any document you file — rulesets revise, and &#39;which rules did this pass?&#39; is what an audit asks years later. &#x60;rulesets&#x60; breaks the same answer down per ruleset. |  |
| **valid** | **Boolean** | Nothing fatal was found. Read it with &#x60;fully_checked&#x60; — on its own it says what was checked came back clean, not that everything was checked. |  |
| **in_scope** | **Boolean** | Whether any of these rulesets is likely to apply to this document at all. False when neither party is in a country that uses one — these are European e-invoicing rulesets, and for a wholly domestic US invoice, say, &#x60;valid&#x60; is answering a question nobody asked. Advisory: it never changes the verdict or withholds the check, because an open network means a US seller invoicing a Dutch buyer genuinely needs it. | [optional][default to true] |
| **fully_checked** | **Boolean** | Every ruleset that applies to this profile ran. False means at least one could not, and &#x60;rulesets&#x60; says which and why. | [optional][default to true] |
| **rulesets** | [**Array&lt;ComplianceRulesetOut&gt;**](ComplianceRulesetOut.md) | Every ruleset the document was held to, including the mandatory-field check, at the version that ran. | [optional] |
| **violations** | [**Array&lt;ComplianceViolationOut&gt;**](ComplianceViolationOut.md) | Every violation found, not the first — fixing one field per round trip is the experience this avoids. Ordered mandatory-field findings first, since those name a field you can go and change. | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ComplianceCheckOut.new(
  profile: peppol_bis_billing_3,
  ruleset_version: EN16931-UBL 1.3.16 + Peppol BIS Billing 3.0.20,
  valid: null,
  in_scope: null,
  fully_checked: null,
  rulesets: null,
  violations: null
)
```

