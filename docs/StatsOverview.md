# InvoicePDFs::StatsOverview

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **counts** | [**StatsCounts**](StatsCounts.md) |  |  |
| **invoice_status_counts** | **Hash&lt;String, Integer&gt;** |  |  |
| **recent_invoices** | [**Array&lt;StatsRecentInvoice&gt;**](StatsRecentInvoice.md) |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::StatsOverview.new(
  counts: null,
  invoice_status_counts: null,
  recent_invoices: null
)
```

