# InvoicePDFs::ImportsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_import**](ImportsApi.md#cancel_import) | **POST** /api/v1/imports/{import_id}/cancel | Cancel Import |
| [**confirm_import**](ImportsApi.md#confirm_import) | **POST** /api/v1/imports/{import_id}/confirm | Confirm Import |
| [**create_import**](ImportsApi.md#create_import) | **POST** /api/v1/imports | Create Import |
| [**get_import**](ImportsApi.md#get_import) | **GET** /api/v1/imports/{import_id} | Get Import |


## cancel_import

> <ImportResponse> cancel_import(import_id)

Cancel Import

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ImportsApi.new
import_id = 'import_id_example' # String | 

begin
  # Cancel Import
  result = api_instance.cancel_import(import_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->cancel_import: #{e}"
end
```

#### Using the cancel_import_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportResponse>, Integer, Hash)> cancel_import_with_http_info(import_id)

```ruby
begin
  # Cancel Import
  data, status_code, headers = api_instance.cancel_import_with_http_info(import_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->cancel_import_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **import_id** | **String** |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## confirm_import

> <ImportResponse> confirm_import(import_id)

Confirm Import

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ImportsApi.new
import_id = 'import_id_example' # String | 

begin
  # Confirm Import
  result = api_instance.confirm_import(import_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->confirm_import: #{e}"
end
```

#### Using the confirm_import_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportResponse>, Integer, Hash)> confirm_import_with_http_info(import_id)

```ruby
begin
  # Confirm Import
  data, status_code, headers = api_instance.confirm_import_with_http_info(import_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->confirm_import_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **import_id** | **String** |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_import

> <ImportResponse> create_import(import_create_request)

Create Import

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ImportsApi.new
import_create_request = InvoicePDFs::ImportCreateRequest.new({source_format: 'json', data: [{ key: 3.56}]}) # ImportCreateRequest | 

begin
  # Create Import
  result = api_instance.create_import(import_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->create_import: #{e}"
end
```

#### Using the create_import_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportResponse>, Integer, Hash)> create_import_with_http_info(import_create_request)

```ruby
begin
  # Create Import
  data, status_code, headers = api_instance.create_import_with_http_info(import_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->create_import_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **import_create_request** | [**ImportCreateRequest**](ImportCreateRequest.md) |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_import

> <ImportResponse> get_import(import_id)

Get Import

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ImportsApi.new
import_id = 'import_id_example' # String | 

begin
  # Get Import
  result = api_instance.get_import(import_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->get_import: #{e}"
end
```

#### Using the get_import_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ImportResponse>, Integer, Hash)> get_import_with_http_info(import_id)

```ruby
begin
  # Get Import
  data, status_code, headers = api_instance.get_import_with_http_info(import_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ImportResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ImportsApi->get_import_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **import_id** | **String** |  |  |

### Return type

[**ImportResponse**](ImportResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

