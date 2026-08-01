# InvoicePDFs::ApiKeysApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_api_key_api_v1_api_keys_post**](ApiKeysApi.md#create_api_key_api_v1_api_keys_post) | **POST** /api/v1/api-keys | Create Api Key |
| [**get_api_key_api_v1_api_keys_api_key_id_get**](ApiKeysApi.md#get_api_key_api_v1_api_keys_api_key_id_get) | **GET** /api/v1/api-keys/{api_key_id} | Get Api Key |
| [**list_api_keys_api_v1_api_keys_get**](ApiKeysApi.md#list_api_keys_api_v1_api_keys_get) | **GET** /api/v1/api-keys | List Api Keys |
| [**patch_api_key_api_v1_api_keys_api_key_id_patch**](ApiKeysApi.md#patch_api_key_api_v1_api_keys_api_key_id_patch) | **PATCH** /api/v1/api-keys/{api_key_id} | Patch Api Key |
| [**revoke_api_key_api_v1_api_keys_api_key_id_delete**](ApiKeysApi.md#revoke_api_key_api_v1_api_keys_api_key_id_delete) | **DELETE** /api/v1/api-keys/{api_key_id} | Revoke Api Key |
| [**rotate_api_key_api_v1_api_keys_api_key_id_rotate_post**](ApiKeysApi.md#rotate_api_key_api_v1_api_keys_api_key_id_rotate_post) | **POST** /api/v1/api-keys/{api_key_id}/rotate | Rotate Api Key |


## create_api_key_api_v1_api_keys_post

> <ApiKeyCreateResponse> create_api_key_api_v1_api_keys_post(api_key_create_request)

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
  result = api_instance.create_api_key_api_v1_api_keys_post(api_key_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->create_api_key_api_v1_api_keys_post: #{e}"
end
```

#### Using the create_api_key_api_v1_api_keys_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyCreateResponse>, Integer, Hash)> create_api_key_api_v1_api_keys_post_with_http_info(api_key_create_request)

```ruby
begin
  # Create Api Key
  data, status_code, headers = api_instance.create_api_key_api_v1_api_keys_post_with_http_info(api_key_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyCreateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->create_api_key_api_v1_api_keys_post_with_http_info: #{e}"
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


## get_api_key_api_v1_api_keys_api_key_id_get

> <ApiKeyDetailResponse> get_api_key_api_v1_api_keys_api_key_id_get(api_key_id)

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
  result = api_instance.get_api_key_api_v1_api_keys_api_key_id_get(api_key_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->get_api_key_api_v1_api_keys_api_key_id_get: #{e}"
end
```

#### Using the get_api_key_api_v1_api_keys_api_key_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyDetailResponse>, Integer, Hash)> get_api_key_api_v1_api_keys_api_key_id_get_with_http_info(api_key_id)

```ruby
begin
  # Get Api Key
  data, status_code, headers = api_instance.get_api_key_api_v1_api_keys_api_key_id_get_with_http_info(api_key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->get_api_key_api_v1_api_keys_api_key_id_get_with_http_info: #{e}"
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


## list_api_keys_api_v1_api_keys_get

> <ApiKeyListResponse> list_api_keys_api_v1_api_keys_get

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
  result = api_instance.list_api_keys_api_v1_api_keys_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->list_api_keys_api_v1_api_keys_get: #{e}"
end
```

#### Using the list_api_keys_api_v1_api_keys_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyListResponse>, Integer, Hash)> list_api_keys_api_v1_api_keys_get_with_http_info

```ruby
begin
  # List Api Keys
  data, status_code, headers = api_instance.list_api_keys_api_v1_api_keys_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->list_api_keys_api_v1_api_keys_get_with_http_info: #{e}"
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


## patch_api_key_api_v1_api_keys_api_key_id_patch

> <ApiKeyDetailResponse> patch_api_key_api_v1_api_keys_api_key_id_patch(api_key_id, api_key_patch_request)

Patch Api Key

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
  # Patch Api Key
  result = api_instance.patch_api_key_api_v1_api_keys_api_key_id_patch(api_key_id, api_key_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->patch_api_key_api_v1_api_keys_api_key_id_patch: #{e}"
end
```

#### Using the patch_api_key_api_v1_api_keys_api_key_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyDetailResponse>, Integer, Hash)> patch_api_key_api_v1_api_keys_api_key_id_patch_with_http_info(api_key_id, api_key_patch_request)

```ruby
begin
  # Patch Api Key
  data, status_code, headers = api_instance.patch_api_key_api_v1_api_keys_api_key_id_patch_with_http_info(api_key_id, api_key_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->patch_api_key_api_v1_api_keys_api_key_id_patch_with_http_info: #{e}"
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


## revoke_api_key_api_v1_api_keys_api_key_id_delete

> <ApiKeyRevokeResponse> revoke_api_key_api_v1_api_keys_api_key_id_delete(api_key_id)

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
  result = api_instance.revoke_api_key_api_v1_api_keys_api_key_id_delete(api_key_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->revoke_api_key_api_v1_api_keys_api_key_id_delete: #{e}"
end
```

#### Using the revoke_api_key_api_v1_api_keys_api_key_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyRevokeResponse>, Integer, Hash)> revoke_api_key_api_v1_api_keys_api_key_id_delete_with_http_info(api_key_id)

```ruby
begin
  # Revoke Api Key
  data, status_code, headers = api_instance.revoke_api_key_api_v1_api_keys_api_key_id_delete_with_http_info(api_key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyRevokeResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->revoke_api_key_api_v1_api_keys_api_key_id_delete_with_http_info: #{e}"
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


## rotate_api_key_api_v1_api_keys_api_key_id_rotate_post

> <ApiKeyRotateResponse> rotate_api_key_api_v1_api_keys_api_key_id_rotate_post(api_key_id)

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
  result = api_instance.rotate_api_key_api_v1_api_keys_api_key_id_rotate_post(api_key_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->rotate_api_key_api_v1_api_keys_api_key_id_rotate_post: #{e}"
end
```

#### Using the rotate_api_key_api_v1_api_keys_api_key_id_rotate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<ApiKeyRotateResponse>, Integer, Hash)> rotate_api_key_api_v1_api_keys_api_key_id_rotate_post_with_http_info(api_key_id)

```ruby
begin
  # Rotate Api Key
  data, status_code, headers = api_instance.rotate_api_key_api_v1_api_keys_api_key_id_rotate_post_with_http_info(api_key_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <ApiKeyRotateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ApiKeysApi->rotate_api_key_api_v1_api_keys_api_key_id_rotate_post_with_http_info: #{e}"
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

