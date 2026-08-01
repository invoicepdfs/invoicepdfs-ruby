# InvoicePDFs::NumberingSequenceCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **prefix** | **String** |  | [optional][default to &#39;INV-&#39;] |
| **date_pattern** | **String** |  | [optional][default to &#39;{YYYY}-&#39;] |
| **padding** | **Integer** |  | [optional][default to 5] |
| **next_number** | **Integer** |  | [optional][default to 1] |
| **reset** | **String** |  | [optional][default to &#39;yearly&#39;] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::NumberingSequenceCreateRequest.new(
  name: Default invoice sequence,
  document_type: null,
  prefix: INV-,
  date_pattern: {YYYY}-,
  padding: 5,
  next_number: 1001,
  reset: null
)
```

