# InvoicePDFs::ApiKeysApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_api_key**](ApiKeysApi.md#create_api_key) | **POST** /api/v1/api-keys | Create Api Key |
| [**get_api_key**](ApiKeysApi.md#get_api_key) | **GET** /api/v1/api-keys/{api_key_id} | Get Api Key |
| [**list_api_keys**](ApiKeysApi.md#list_api_keys) | **GET** /api/v1/api-keys | List Api Keys |
| [**revoke_api_key**](ApiKeysApi.md#revoke_api_key) | **DELETE** /api/v1/api-keys/{api_key_id} | Revoke Api Key |
| [**rotate_api_key**](ApiKeysApi.md#rotate_api_key) | **POST** /api/v1/api-keys/{api_key_id}/rotate | Rotate Api Key |
| [**update_api_key**](ApiKeysApi.md#update_api_key) | **PATCH** /api/v1/api-keys/{api_key_id} | Update Api Key |


## create_api_key

> <ApiKeyCreateResponse> create_api_key(api_key_create_request)

Create Api Key

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ApiKeysApi.new
api_key_create_request = InvoicePDFs::ApiKeyCreateRequest.new # ApiKeyCreateRequest | 

begin
  # Create Api Key
  result = api_instance.create_api_key(api_key_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->create_api_key: #{e}"
end
```

#### Using the create_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyCreateResponse>, Integer, Hash)> create_api_key_with_http_info(api_key_create_request)

```ruby
begin
  # Create Api Key
  data, status_code, headers = api_instance.create_api_key_with_http_info(api_key_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyCreateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->create_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_key_create_request** | [**ApiKeyCreateRequest**](ApiKeyCreateRequest.md) |  |  |

### Return type

[**ApiKeyCreateResponse**](ApiKeyCreateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_api_key

> <ApiKeyDetailResponse> get_api_key(api_key_id)

Get Api Key

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ApiKeysApi.new
api_key_id = 'api_key_id_example' # String | 

begin
  # Get Api Key
  result = api_instance.get_api_key(api_key_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->get_api_key: #{e}"
end
```

#### Using the get_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyDetailResponse>, Integer, Hash)> get_api_key_with_http_info(api_key_id)

```ruby
begin
  # Get Api Key
  data, status_code, headers = api_instance.get_api_key_with_http_info(api_key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->get_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_key_id** | **String** |  |  |

### Return type

[**ApiKeyDetailResponse**](ApiKeyDetailResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_api_keys

> <ApiKeyListResponse> list_api_keys

List Api Keys

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ApiKeysApi.new

begin
  # List Api Keys
  result = api_instance.list_api_keys
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->list_api_keys: #{e}"
end
```

#### Using the list_api_keys_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyListResponse>, Integer, Hash)> list_api_keys_with_http_info

```ruby
begin
  # List Api Keys
  data, status_code, headers = api_instance.list_api_keys_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->list_api_keys_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**ApiKeyListResponse**](ApiKeyListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## revoke_api_key

> <ApiKeyRevokeResponse> revoke_api_key(api_key_id)

Revoke Api Key

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ApiKeysApi.new
api_key_id = 'api_key_id_example' # String | 

begin
  # Revoke Api Key
  result = api_instance.revoke_api_key(api_key_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->revoke_api_key: #{e}"
end
```

#### Using the revoke_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyRevokeResponse>, Integer, Hash)> revoke_api_key_with_http_info(api_key_id)

```ruby
begin
  # Revoke Api Key
  data, status_code, headers = api_instance.revoke_api_key_with_http_info(api_key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyRevokeResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->revoke_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_key_id** | **String** |  |  |

### Return type

[**ApiKeyRevokeResponse**](ApiKeyRevokeResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## rotate_api_key

> <ApiKeyRotateResponse> rotate_api_key(api_key_id)

Rotate Api Key

Revoke the existing key and create a new one with the same name.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ApiKeysApi.new
api_key_id = 'api_key_id_example' # String | 

begin
  # Rotate Api Key
  result = api_instance.rotate_api_key(api_key_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->rotate_api_key: #{e}"
end
```

#### Using the rotate_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyRotateResponse>, Integer, Hash)> rotate_api_key_with_http_info(api_key_id)

```ruby
begin
  # Rotate Api Key
  data, status_code, headers = api_instance.rotate_api_key_with_http_info(api_key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyRotateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->rotate_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_key_id** | **String** |  |  |

### Return type

[**ApiKeyRotateResponse**](ApiKeyRotateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_api_key

> <ApiKeyDetailResponse> update_api_key(api_key_id, api_key_patch_request)

Update Api Key

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ApiKeysApi.new
api_key_id = 'api_key_id_example' # String | 
api_key_patch_request = InvoicePDFs::ApiKeyPatchRequest.new({name: 'name_example'}) # ApiKeyPatchRequest | 

begin
  # Update Api Key
  result = api_instance.update_api_key(api_key_id, api_key_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->update_api_key: #{e}"
end
```

#### Using the update_api_key_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyDetailResponse>, Integer, Hash)> update_api_key_with_http_info(api_key_id, api_key_patch_request)

```ruby
begin
  # Update Api Key
  data, status_code, headers = api_instance.update_api_key_with_http_info(api_key_id, api_key_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->update_api_key_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **api_key_id** | **String** |  |  |
| **api_key_patch_request** | [**ApiKeyPatchRequest**](ApiKeyPatchRequest.md) |  |  |

### Return type

[**ApiKeyDetailResponse**](ApiKeyDetailResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

