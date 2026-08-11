# InvoicePDFs::TemplateVersionsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_template_version**](TemplateVersionsApi.md#create_template_version) | **POST** /api/v1/templates/{template_id}/versions | Create Template Version |
| [**get_template_version**](TemplateVersionsApi.md#get_template_version) | **GET** /api/v1/templates/{template_id}/versions/{version} | Get Template Version |
| [**list_template_versions**](TemplateVersionsApi.md#list_template_versions) | **GET** /api/v1/templates/{template_id}/versions | List Template Versions |


## create_template_version

> <TemplateVersionResponse> create_template_version(template_id, template_version_create_request)

Create Template Version

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplateVersionsApi.new
template_id = 'template_id_example' # String | 
template_version_create_request = InvoicePDFs::TemplateVersionCreateRequest.new # TemplateVersionCreateRequest | 

begin
  # Create Template Version
  result = api_instance.create_template_version(template_id, template_version_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplateVersionsApi->create_template_version: #{e}"
end
```

#### Using the create_template_version_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplateVersionResponse>, Integer, Hash)> create_template_version_with_http_info(template_id, template_version_create_request)

```ruby
begin
  # Create Template Version
  data, status_code, headers = api_instance.create_template_version_with_http_info(template_id, template_version_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplateVersionResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplateVersionsApi->create_template_version_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |
| **template_version_create_request** | [**TemplateVersionCreateRequest**](TemplateVersionCreateRequest.md) |  |  |

### Return type

[**TemplateVersionResponse**](TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_template_version

> <TemplateVersionResponse> get_template_version(template_id, version)

Get Template Version

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplateVersionsApi.new
template_id = 'template_id_example' # String | 
version = 56 # Integer | 

begin
  # Get Template Version
  result = api_instance.get_template_version(template_id, version)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplateVersionsApi->get_template_version: #{e}"
end
```

#### Using the get_template_version_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplateVersionResponse>, Integer, Hash)> get_template_version_with_http_info(template_id, version)

```ruby
begin
  # Get Template Version
  data, status_code, headers = api_instance.get_template_version_with_http_info(template_id, version)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplateVersionResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplateVersionsApi->get_template_version_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |
| **version** | **Integer** |  |  |

### Return type

[**TemplateVersionResponse**](TemplateVersionResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_template_versions

> <TemplateVersionsListResponse> list_template_versions(template_id)

List Template Versions

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplateVersionsApi.new
template_id = 'template_id_example' # String | 

begin
  # List Template Versions
  result = api_instance.list_template_versions(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplateVersionsApi->list_template_versions: #{e}"
end
```

#### Using the list_template_versions_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplateVersionsListResponse>, Integer, Hash)> list_template_versions_with_http_info(template_id)

```ruby
begin
  # List Template Versions
  data, status_code, headers = api_instance.list_template_versions_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplateVersionsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplateVersionsApi->list_template_versions_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

[**TemplateVersionsListResponse**](TemplateVersionsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

