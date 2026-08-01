# InvoicePDFs::InvoicePatchRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_number** | **String** |  | [optional] |
| **document_type** | **String** |  | [optional] |
| **issue_date** | **Date** |  | [optional] |
| **due_date** | **Date** |  | [optional] |
| **currency** | **String** |  | [optional] |
| **locale** | **String** |  | [optional] |
| **business_profile_id** | **String** |  | [optional] |
| **customer_id** | **String** |  | [optional] |
| **ship_to** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **line_items** | [**Array&lt;InvoiceLineItemInput&gt;**](InvoiceLineItemInput.md) |  | [optional] |
| **discounts** | [**Array&lt;InvoiceDiscountInput&gt;**](InvoiceDiscountInput.md) |  | [optional] |
| **shipping** | [**InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional] |
| **notes** | [**Array&lt;InvoiceNoteInput&gt;**](InvoiceNoteInput.md) |  | [optional] |
| **terms** | [**Array&lt;InvoiceTermInput&gt;**](InvoiceTermInput.md) |  | [optional] |
| **custom_fields** | [**Array&lt;InvoiceCustomFieldInput&gt;**](InvoiceCustomFieldInput.md) |  | [optional] |
| **payment** | [**InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional] |
| **branding** | [**InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::InvoicePatchRequest.new(
  invoice_number: null,
  document_type: null,
  issue_date: null,
  due_date: null,
  currency: null,
  locale: null,
  business_profile_id: null,
  customer_id: null,
  ship_to: null,
  line_items: null,
  discounts: null,
  shipping: null,
  notes: null,
  terms: null,
  custom_fields: null,
  payment: null,
  branding: null
)
```

