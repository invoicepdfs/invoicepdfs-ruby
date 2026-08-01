# InvoicePDFs::StatsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_stats_api_v1_stats_get**](StatsApi.md#get_stats_api_v1_stats_get) | **GET** /api/v1/stats | Get Stats |


## get_stats_api_v1_stats_get

> <StatsResponse> get_stats_api_v1_stats_get

Get Stats

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::StatsApi.new

begin
  # Get Stats
  result = api_instance.get_stats_api_v1_stats_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling StatsApi->get_stats_api_v1_stats_get: #{e}"
end
```

#### Using the get_stats_api_v1_stats_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<StatsResponse>, Integer, Hash)> get_stats_api_v1_stats_get_with_http_info

```ruby
begin
  # Get Stats
  data, status_code, headers = api_instance.get_stats_api_v1_stats_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <StatsResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling StatsApi->get_stats_api_v1_stats_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**StatsResponse**](StatsResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

