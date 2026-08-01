# InvoicePDFs::DocumentInvoiceDataInput

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_number** | **String** |  |  |
| **issue_date** | **Date** |  |  |
| **due_date** | **Date** |  | [optional] |
| **currency** | **String** |  |  |
| **seller** | [**DocumentPartyInput**](DocumentPartyInput.md) |  |  |
| **buyer** | [**DocumentPartyInput**](DocumentPartyInput.md) |  |  |
| **ship_to** | [**DocumentPartyInput**](DocumentPartyInput.md) |  | [optional] |
| **line_items** | [**Array&lt;DocumentLineItemInput&gt;**](DocumentLineItemInput.md) |  |  |
| **discounts** | [**Array&lt;DocumentDiscountInput&gt;**](DocumentDiscountInput.md) |  | [optional] |
| **shipping** | [**DocumentShippingInput**](DocumentShippingInput.md) |  | [optional] |
| **custom_fields** | [**Array&lt;DocumentCustomFieldInput&gt;**](DocumentCustomFieldInput.md) |  | [optional] |
| **payment** | [**DocumentPaymentInput**](DocumentPaymentInput.md) |  | [optional] |
| **branding** | [**DocumentBrandingInput**](DocumentBrandingInput.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentInvoiceDataInput.new(
  invoice_number: INV-2026-001,
  issue_date: Mon Jul 20 00:00:00 UTC 2026,
  due_date: null,
  currency: USD,
  seller: null,
  buyer: null,
  ship_to: null,
  line_items: null,
  discounts: null,
  shipping: null,
  custom_fields: null,
  payment: null,
  branding: null
)
```

