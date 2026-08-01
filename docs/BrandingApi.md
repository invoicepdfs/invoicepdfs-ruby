# InvoicePDFs::BrandingApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_logo_api_v1_branding_logo_delete**](BrandingApi.md#delete_logo_api_v1_branding_logo_delete) | **DELETE** /api/v1/branding/logo | Delete Logo |
| [**get_branding_api_v1_branding_get**](BrandingApi.md#get_branding_api_v1_branding_get) | **GET** /api/v1/branding | Get Branding |
| [**update_branding_api_v1_branding_put**](BrandingApi.md#update_branding_api_v1_branding_put) | **PUT** /api/v1/branding | Update Branding |
| [**upload_logo_api_v1_branding_logo_post**](BrandingApi.md#upload_logo_api_v1_branding_logo_post) | **POST** /api/v1/branding/logo | Upload Logo |


## delete_logo_api_v1_branding_logo_delete

> <SimpleBoolResponse> delete_logo_api_v1_branding_logo_delete

Delete Logo

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingApi.new

begin
  # Delete Logo
  result = api_instance.delete_logo_api_v1_branding_logo_delete
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->delete_logo_api_v1_branding_logo_delete: #{e}"
end
```

#### Using the delete_logo_api_v1_branding_logo_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_logo_api_v1_branding_logo_delete_with_http_info

```ruby
begin
  # Delete Logo
  data, status_code, headers = api_instance.delete_logo_api_v1_branding_logo_delete_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->delete_logo_api_v1_branding_logo_delete_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_branding_api_v1_branding_get

> <BrandingResponse> get_branding_api_v1_branding_get

Get Branding

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingApi.new

begin
  # Get Branding
  result = api_instance.get_branding_api_v1_branding_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->get_branding_api_v1_branding_get: #{e}"
end
```

#### Using the get_branding_api_v1_branding_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingResponse>, Integer, Hash)> get_branding_api_v1_branding_get_with_http_info

```ruby
begin
  # Get Branding
  data, status_code, headers = api_instance.get_branding_api_v1_branding_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->get_branding_api_v1_branding_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BrandingResponse**](BrandingResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_branding_api_v1_branding_put

> <BrandingResponse> update_branding_api_v1_branding_put(branding_update_request)

Update Branding

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingApi.new
branding_update_request = InvoicePDFs::BrandingUpdateRequest.new # BrandingUpdateRequest | 

begin
  # Update Branding
  result = api_instance.update_branding_api_v1_branding_put(branding_update_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->update_branding_api_v1_branding_put: #{e}"
end
```

#### Using the update_branding_api_v1_branding_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingResponse>, Integer, Hash)> update_branding_api_v1_branding_put_with_http_info(branding_update_request)

```ruby
begin
  # Update Branding
  data, status_code, headers = api_instance.update_branding_api_v1_branding_put_with_http_info(branding_update_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->update_branding_api_v1_branding_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **branding_update_request** | [**BrandingUpdateRequest**](BrandingUpdateRequest.md) |  |  |

### Return type

[**BrandingResponse**](BrandingResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## upload_logo_api_v1_branding_logo_post

> <BrandingResponse> upload_logo_api_v1_branding_logo_post(file)

Upload Logo

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingApi.new
file = File.new('/path/to/some/file') # File | 

begin
  # Upload Logo
  result = api_instance.upload_logo_api_v1_branding_logo_post(file)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->upload_logo_api_v1_branding_logo_post: #{e}"
end
```

#### Using the upload_logo_api_v1_branding_logo_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingResponse>, Integer, Hash)> upload_logo_api_v1_branding_logo_post_with_http_info(file)

```ruby
begin
  # Upload Logo
  data, status_code, headers = api_instance.upload_logo_api_v1_branding_logo_post_with_http_info(file)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingApi->upload_logo_api_v1_branding_logo_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file** | **File** |  |  |

### Return type

[**BrandingResponse**](BrandingResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

