# InvoicePDFs::UsageApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_usage**](UsageApi.md#get_usage) | **GET** /api/v1/usage | Get Usage |
| [**get_usage_limits**](UsageApi.md#get_usage_limits) | **GET** /api/v1/usage/limits | Get Usage Limits |
| [**list_usage_events**](UsageApi.md#list_usage_events) | **GET** /api/v1/usage/events | List Usage Events |


## get_usage

> <UsageResponse> get_usage

Get Usage

Renders used this calendar month, against the plan's quota.  The period starts at midnight UTC on the first of the month.  For rate limits, log retention and overage, use `get_usage_limits`; for the individual renders behind the count, `list_usage_events`.

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
  # Get Usage
  result = api_instance.get_usage
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->get_usage: #{e}"
end
```

#### Using the get_usage_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UsageResponse>, Integer, Hash)> get_usage_with_http_info

```ruby
begin
  # Get Usage
  data, status_code, headers = api_instance.get_usage_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UsageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->get_usage_with_http_info: #{e}"
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


## get_usage_limits

> <UsageLimitsResponse> get_usage_limits

Get Usage Limits

Every ceiling on the account, and how close you are to each.  A superset of `get_usage`: the render quota and what is left of it, plus requests per second, how long API logs are kept, and overage — whether it is enabled and available on the plan, how many renders have gone over, and what they have cost so far.  The cost estimate is rounded up, so it is never lower than the invoice.

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
  # Get Usage Limits
  result = api_instance.get_usage_limits
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->get_usage_limits: #{e}"
end
```

#### Using the get_usage_limits_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UsageLimitsResponse>, Integer, Hash)> get_usage_limits_with_http_info

```ruby
begin
  # Get Usage Limits
  data, status_code, headers = api_instance.get_usage_limits_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UsageLimitsResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->get_usage_limits_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**UsageLimitsResponse**](UsageLimitsResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_usage_events

> <UsageEventsListResponse> list_usage_events(opts)

List Usage Events

One row per metered render, newest first.  The detail behind the count `get_usage` returns, each row naming the render that produced it.

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
  result = api_instance.list_usage_events(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->list_usage_events: #{e}"
end
```

#### Using the list_usage_events_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<UsageEventsListResponse>, Integer, Hash)> list_usage_events_with_http_info(opts)

```ruby
begin
  # List Usage Events
  data, status_code, headers = api_instance.list_usage_events_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <UsageEventsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling UsageApi->list_usage_events_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**UsageEventsListResponse**](UsageEventsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

