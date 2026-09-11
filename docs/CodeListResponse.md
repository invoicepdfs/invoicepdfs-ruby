# InvoicePDFs::CodeListResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **data** | [**Array&lt;CodeOut&gt;**](CodeOut.md) |  |  |
| **standard** | **String** | The code list these values come from. |  |
| **exhaustive** | **Boolean** | Whether &#x60;data&#x60; is the complete list. When false it is a shortlist and other codes remain valid. |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::CodeListResponse.new(
  data: null,
  standard: UN/ECE Recommendation 20,
  exhaustive: null
)
```

