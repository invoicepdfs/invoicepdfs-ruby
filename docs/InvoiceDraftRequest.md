# InvoicePDFs::InvoiceDraftRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_number** | **String** |  |  |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **issue_date** | **Date** |  |  |
| **due_date** | **Date** |  | [optional] |
| **currency** | **String** |  |  |
| **locale** | **String** |  | [optional] |
| **business_profile_id** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **ship_to** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **line_items** | [**Array&lt;InvoiceLineItemInput&gt;**](InvoiceLineItemInput.md) |  |  |
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

instance = InvoicePDFs::InvoiceDraftRequest.new(
  invoice_number: INV-2026-001,
  document_type: null,
  issue_date: Mon Jul 20 00:00:00 UTC 2026,
  due_date: null,
  currency: USD,
  locale: null,
  business_profile_id: bp_01ABC,
  customer_id: cus_01XYZ,
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

