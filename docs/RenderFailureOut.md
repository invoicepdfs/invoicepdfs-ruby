# InvoicePDFs::RenderFailureOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | &#x60;compliance_failed&#x60; for a document that is well-formed and would be rejected by the ruleset it asked for; &#x60;unprocessable_entity&#x60; for one the renderer could not make sense of. The same codes the synchronous path returns. |  |
| **message** | **String** |  |  |
| **details** | **Hash&lt;String, Object&gt;** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::RenderFailureOut.new(
  code: compliance_failed,
  message: null,
  details: null
)
```

