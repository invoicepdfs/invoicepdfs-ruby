# InvoicePDFs::BatchCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **operation** | **String** |  | [optional][default to &#39;render&#39;] |
| **items** | [**Array&lt;BatchItemInput&gt;**](BatchItemInput.md) |  |  |
| **template_id** | **String** |  | [optional][default to &#39;tpl_modern&#39;] |
| **output** | [**BatchOutputOptions**](BatchOutputOptions.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::BatchCreateRequest.new(
  operation: null,
  items: null,
  template_id: null,
  output: null
)
```

