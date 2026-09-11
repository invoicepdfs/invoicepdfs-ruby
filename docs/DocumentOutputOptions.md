# InvoicePDFs::DocumentOutputOptions

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **format** | **String** |  | [optional][default to &#39;pdf&#39;] |
| **delivery** | **String** |  | [optional][default to &#39;url&#39;] |
| **expires_in** | **Integer** | How long the render stays downloadable, in seconds (1 minute to 7 days). It is also the lifetime of the signature in &#x60;download_url&#x60;, which is why it is bounded: an unbounded value meant an unbounded grant. A value below the floor used to be accepted and produced a render that had already expired. | [optional][default to 3600] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentOutputOptions.new(
  format: null,
  delivery: null,
  expires_in: null
)
```

