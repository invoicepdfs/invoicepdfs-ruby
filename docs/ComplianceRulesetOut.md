# InvoicePDFs::ComplianceRulesetOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **label** | **String** |  |  |
| **version** | **String** | The upstream release of the rules. Empty for checks with no version of their own. | [optional][default to &#39;&#39;] |
| **ran** | **Boolean** | False when this ruleset could not be run at all. A ruleset that did not run is not a pass — &#x60;valid&#x60; only reports what was checked. |  |
| **reason** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::ComplianceRulesetOut.new(
  id: peppol-en16931-ubl,
  label: Peppol BIS Billing 3.0,
  version: 3.0.20,
  ran: null,
  reason: null
)
```

