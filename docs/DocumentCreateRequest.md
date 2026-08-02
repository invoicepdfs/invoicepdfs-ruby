# InvoicePDFs::DocumentCreateRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_type** | **String** |  | [optional][default to &#39;invoice&#39;] |
| **number** | **String** |  |  |
| **issue_date** | **Date** |  |  |
| **due_date** | **Date** |  | [optional] |
| **currency** | **String** |  |  |
| **locale** | **String** |  | [optional] |
| **business_profile_id** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **source_document_id** | **String** |  | [optional] |
| **reason** | **String** |  | [optional] |
| **ship_to** | [**PostalAddress**](PostalAddress.md) |  | [optional] |
| **line_items** | [**Array&lt;StandardLineItemInput&gt;**](StandardLineItemInput.md) |  |  |
| **discounts** | [**Array&lt;LineItemDiscountInput&gt;**](LineItemDiscountInput.md) |  | [optional] |
| **shipping** | [**InvoiceShippingInput**](InvoiceShippingInput.md) |  | [optional] |
| **notes** | [**Array&lt;InvoiceNoteInput&gt;**](InvoiceNoteInput.md) |  | [optional] |
| **terms** | [**Array&lt;InvoiceTermInput&gt;**](InvoiceTermInput.md) |  | [optional] |
| **custom_fields** | [**Array&lt;InvoiceCustomFieldInput&gt;**](InvoiceCustomFieldInput.md) |  | [optional] |
| **payment** | [**InvoicePaymentInput**](InvoicePaymentInput.md) |  | [optional] |
| **branding** | [**InvoiceBrandingInput**](InvoiceBrandingInput.md) |  | [optional] |
| **branding_profile_id** | **String** |  | [optional] |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::DocumentCreateRequest.new(
  document_type: null,
  number: INV-2026-001,
  issue_date: Mon Jul 20 00:00:00 UTC 2026,
  due_date: null,
  currency: USD,
  locale: null,
  business_profile_id: bp_01ABC,
  customer_id: cus_01XYZ,
  source_document_id: null,
  reason: null,
  ship_to: null,
  line_items: null,
  discounts: null,
  shipping: null,
  notes: null,
  terms: null,
  custom_fields: null,
  payment: null,
  branding: null,
  branding_profile_id: null
)
```

