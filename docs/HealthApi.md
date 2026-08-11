# InvoicePDFs::HealthApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_health**](HealthApi.md#get_health) | **GET** /health | Get Health |
| [**get_readiness**](HealthApi.md#get_readiness) | **GET** /ready | Get Readiness |
| [**get_version**](HealthApi.md#get_version) | **GET** /version | Get Version |


## get_health

> <HealthResponse> get_health

Get Health

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::HealthApi.new

begin
  # Get Health
  result = api_instance.get_health
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->get_health: #{e}"
end
```

#### Using the get_health_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<HealthResponse>, Integer, Hash)> get_health_with_http_info

```ruby
begin
  # Get Health
  data, status_code, headers = api_instance.get_health_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <HealthResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->get_health_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**HealthResponse**](HealthResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_readiness

> <ReadyResponse> get_readiness

Get Readiness

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::HealthApi.new

begin
  # Get Readiness
  result = api_instance.get_readiness
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->get_readiness: #{e}"
end
```

#### Using the get_readiness_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReadyResponse>, Integer, Hash)> get_readiness_with_http_info

```ruby
begin
  # Get Readiness
  data, status_code, headers = api_instance.get_readiness_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReadyResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->get_readiness_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ReadyResponse**](ReadyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_version

> <VersionResponse> get_version

Get Version

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::HealthApi.new

begin
  # Get Version
  result = api_instance.get_version
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->get_version: #{e}"
end
```

#### Using the get_version_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VersionResponse>, Integer, Hash)> get_version_with_http_info

```ruby
begin
  # Get Version
  data, status_code, headers = api_instance.get_version_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VersionResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->get_version_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**VersionResponse**](VersionResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

