# InvoicePDFs::DeliveryOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **invoice_id** | **String** |  |  |
| **to** | **Array&lt;String&gt;** |  |  |
| **cc** | **Array&lt;String&gt;** |  |  |
| **bcc** | **Array&lt;String&gt;** |  |  |
| **subject** | **String** |  |  |
| **message** | **String** |  | [optional] |
| **attach_pdf** | **Boolean** |  |  |
| **status** | **String** |  |  |
| **created_at** | **String** |  |  |
| **sent_at** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DeliveryOut.new(
  id: null,
  invoice_id: null,
  to: null,
  cc: null,
  bcc: null,
  subject: null,
  message: null,
  attach_pdf: null,
  status: null,
  created_at: null,
  sent_at: null
)
```

