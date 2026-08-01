# InvoicePDFs::UsageApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_limits_api_v1_usage_limits_get**](UsageApi.md#get_limits_api_v1_usage_limits_get) | **GET** /api/v1/usage/limits | Get Limits |
| [**list_usage_events_api_v1_usage_events_get**](UsageApi.md#list_usage_events_api_v1_usage_events_get) | **GET** /api/v1/usage/events | List Usage Events |
| [**usage_api_v1_usage_get**](UsageApi.md#usage_api_v1_usage_get) | **GET** /api/v1/usage | Usage |


## get_limits_api_v1_usage_limits_get

> Hash&lt;String, Object&gt; get_limits_api_v1_usage_limits_get

Get Limits

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::UsageApi.new

begin
  # Get Limits
  result = api_instance.get_limits_api_v1_usage_limits_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->get_limits_api_v1_usage_limits_get: #{e}"
end
```

#### Using the get_limits_api_v1_usage_limits_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> get_limits_api_v1_usage_limits_get_with_http_info

```ruby
begin
  # Get Limits
  data, status_code, headers = api_instance.get_limits_api_v1_usage_limits_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->get_limits_api_v1_usage_limits_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_usage_events_api_v1_usage_events_get

> Hash&lt;String, Object&gt; list_usage_events_api_v1_usage_events_get(opts)

List Usage Events

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::UsageApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Usage Events
  result = api_instance.list_usage_events_api_v1_usage_events_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->list_usage_events_api_v1_usage_events_get: #{e}"
end
```

#### Using the list_usage_events_api_v1_usage_events_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> list_usage_events_api_v1_usage_events_get_with_http_info(opts)

```ruby
begin
  # List Usage Events
  data, status_code, headers = api_instance.list_usage_events_api_v1_usage_events_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->list_usage_events_api_v1_usage_events_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## usage_api_v1_usage_get

> <UsageResponse> usage_api_v1_usage_get

Usage

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::UsageApi.new

begin
  # Usage
  result = api_instance.usage_api_v1_usage_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->usage_api_v1_usage_get: #{e}"
end
```

#### Using the usage_api_v1_usage_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UsageResponse>, Integer, Hash)> usage_api_v1_usage_get_with_http_info

```ruby
begin
  # Usage
  data, status_code, headers = api_instance.usage_api_v1_usage_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UsageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->usage_api_v1_usage_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**UsageResponse**](UsageResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

