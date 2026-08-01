# InvoicePDFs::HealthApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**health_health_get**](HealthApi.md#health_health_get) | **GET** /health | Health |
| [**ready_ready_get**](HealthApi.md#ready_ready_get) | **GET** /ready | Ready |
| [**version_version_get**](HealthApi.md#version_version_get) | **GET** /version | Version |


## health_health_get

> <HealthResponse> health_health_get

Health

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::HealthApi.new

begin
  # Health
  result = api_instance.health_health_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->health_health_get: #{e}"
end
```

#### Using the health_health_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<HealthResponse>, Integer, Hash)> health_health_get_with_http_info

```ruby
begin
  # Health
  data, status_code, headers = api_instance.health_health_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <HealthResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->health_health_get_with_http_info: #{e}"
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


## ready_ready_get

> <ReadyResponse> ready_ready_get

Ready

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::HealthApi.new

begin
  # Ready
  result = api_instance.ready_ready_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->ready_ready_get: #{e}"
end
```

#### Using the ready_ready_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ReadyResponse>, Integer, Hash)> ready_ready_get_with_http_info

```ruby
begin
  # Ready
  data, status_code, headers = api_instance.ready_ready_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ReadyResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->ready_ready_get_with_http_info: #{e}"
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


## version_version_get

> <VersionResponse> version_version_get

Version

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::HealthApi.new

begin
  # Version
  result = api_instance.version_version_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->version_version_get: #{e}"
end
```

#### Using the version_version_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<VersionResponse>, Integer, Hash)> version_version_get_with_http_info

```ruby
begin
  # Version
  data, status_code, headers = api_instance.version_version_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <VersionResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling HealthApi->version_version_get_with_http_info: #{e}"
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

