# InvoicePDFs::LogsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_logs**](LogsApi.md#list_logs) | **GET** /api/v1/logs | List Logs |


## list_logs

> <ApiRequestLogsListResponse> list_logs(opts)

List Logs

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::LogsApi.new
opts = {
  status: 'status_example', # String | 
  limit: 56 # Integer | 
}

begin
  # List Logs
  result = api_instance.list_logs(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling LogsApi->list_logs: #{e}"
end
```

#### Using the list_logs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiRequestLogsListResponse>, Integer, Hash)> list_logs_with_http_info(opts)

```ruby
begin
  # List Logs
  data, status_code, headers = api_instance.list_logs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiRequestLogsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling LogsApi->list_logs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** |  | [optional][default to &#39;&#39;] |
| **limit** | **Integer** |  | [optional][default to 100] |

### Return type

[**ApiRequestLogsListResponse**](ApiRequestLogsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

