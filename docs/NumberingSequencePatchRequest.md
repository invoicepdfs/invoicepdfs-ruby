# InvoicePDFs::NumberingSequencePatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  | [optional] |
| **prefix** | **String** |  | [optional] |
| **date_pattern** | **String** |  | [optional] |
| **padding** | **Integer** |  | [optional] |
| **next_number** | **Integer** |  | [optional] |
| **reset** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::NumberingSequencePatchRequest.new(
  name: null,
  prefix: null,
  date_pattern: null,
  padding: null,
  next_number: null,
  reset: null
)
```

