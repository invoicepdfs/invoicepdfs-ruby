# InvoicePDFs::AuditLogApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_audit_event**](AuditLogApi.md#get_audit_event) | **GET** /api/v1/audit-events/{audit_event_id} | Get Audit Event |
| [**list_audit_events**](AuditLogApi.md#list_audit_events) | **GET** /api/v1/audit-events | List Audit Events |


## get_audit_event

> <AuditEventResponse> get_audit_event(audit_event_id)

Get Audit Event

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::AuditLogApi.new
audit_event_id = 'audit_event_id_example' # String | 

begin
  # Get Audit Event
  result = api_instance.get_audit_event(audit_event_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuditLogApi->get_audit_event: #{e}"
end
```

#### Using the get_audit_event_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuditEventResponse>, Integer, Hash)> get_audit_event_with_http_info(audit_event_id)

```ruby
begin
  # Get Audit Event
  data, status_code, headers = api_instance.get_audit_event_with_http_info(audit_event_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuditEventResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuditLogApi->get_audit_event_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **audit_event_id** | **String** |  |  |

### Return type

[**AuditEventResponse**](AuditEventResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_audit_events

> <AuditEventsListResponse> list_audit_events(opts)

List Audit Events

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::AuditLogApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example', # String | 
  action: 'action_example', # String | 
  resource_type: 'resource_type_example', # String | 
  resource_id: 'resource_id_example' # String | 
}

begin
  # List Audit Events
  result = api_instance.list_audit_events(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuditLogApi->list_audit_events: #{e}"
end
```

#### Using the list_audit_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuditEventsListResponse>, Integer, Hash)> list_audit_events_with_http_info(opts)

```ruby
begin
  # List Audit Events
  data, status_code, headers = api_instance.list_audit_events_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuditEventsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuditLogApi->list_audit_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |
| **action** | **String** |  | [optional] |
| **resource_type** | **String** |  | [optional] |
| **resource_id** | **String** |  | [optional] |

### Return type

[**AuditEventsListResponse**](AuditEventsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

