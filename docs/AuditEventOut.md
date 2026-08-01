# InvoicePDFs::AuditEventOut

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **actor** | **String** |  |  |
| **action** | **String** |  |  |
| **resource_type** | **String** |  |  |
| **resource_id** | **String** |  |  |
| **workspace_id** | **String** |  | [optional] |
| **ip_address** | **String** |  | [optional] |
| **user_agent** | **String** |  | [optional] |
| **request_id** | **String** |  | [optional] |
| **summary** | **String** |  | [optional] |
| **created_at** | **String** |  |  |

## Example

```ruby
require 'invoicepdfs'

instance = InvoicePDFs::AuditEventOut.new(
  id: null,
  actor: null,
  action: null,
  resource_type: null,
  resource_id: null,
  workspace_id: null,
  ip_address: null,
  user_agent: null,
  request_id: null,
  summary: null,
  created_at: null
)
```

