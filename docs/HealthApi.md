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

Is the API process alive.  Answers as long as the process can serve a request; it checks nothing behind it. For whether the service can actually do work, use `get_readiness`.

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

Can the API serve real traffic — dependencies included.  Checks the database, storage, and the separate render service, and reports each one. `status` is `ready` only when all three are `ok`, so this is the check to point a load balancer at. `get_health` answers sooner but proves less.

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

Which build is deployed.

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

