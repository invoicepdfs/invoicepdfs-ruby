# InvoicePDFs::BusinessProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_business_profile_api_v1_business_profiles_post**](BusinessProfilesApi.md#create_business_profile_api_v1_business_profiles_post) | **POST** /api/v1/business-profiles | Create Business Profile |
| [**delete_business_profile_api_v1_business_profiles_business_profile_id_delete**](BusinessProfilesApi.md#delete_business_profile_api_v1_business_profiles_business_profile_id_delete) | **DELETE** /api/v1/business-profiles/{business_profile_id} | Delete Business Profile |
| [**get_business_profile_api_v1_business_profiles_business_profile_id_get**](BusinessProfilesApi.md#get_business_profile_api_v1_business_profiles_business_profile_id_get) | **GET** /api/v1/business-profiles/{business_profile_id} | Get Business Profile |
| [**list_business_profiles_api_v1_business_profiles_get**](BusinessProfilesApi.md#list_business_profiles_api_v1_business_profiles_get) | **GET** /api/v1/business-profiles | List Business Profiles |
| [**patch_business_profile_api_v1_business_profiles_business_profile_id_patch**](BusinessProfilesApi.md#patch_business_profile_api_v1_business_profiles_business_profile_id_patch) | **PATCH** /api/v1/business-profiles/{business_profile_id} | Patch Business Profile |


## create_business_profile_api_v1_business_profiles_post

> <BusinessProfileResponse> create_business_profile_api_v1_business_profiles_post(business_profile_create, opts)

Create Business Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BusinessProfilesApi.new
business_profile_create = InvoicePDFs::BusinessProfileCreate.new({legal_name: 'Acme Corp Inc.'}) # BusinessProfileCreate | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Create Business Profile
  result = api_instance.create_business_profile_api_v1_business_profiles_post(business_profile_create, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->create_business_profile_api_v1_business_profiles_post: #{e}"
end
```

#### Using the create_business_profile_api_v1_business_profiles_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BusinessProfileResponse>, Integer, Hash)> create_business_profile_api_v1_business_profiles_post_with_http_info(business_profile_create, opts)

```ruby
begin
  # Create Business Profile
  data, status_code, headers = api_instance.create_business_profile_api_v1_business_profiles_post_with_http_info(business_profile_create, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BusinessProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->create_business_profile_api_v1_business_profiles_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_profile_create** | [**BusinessProfileCreate**](BusinessProfileCreate.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_business_profile_api_v1_business_profiles_business_profile_id_delete

> <SimpleBoolResponse> delete_business_profile_api_v1_business_profiles_business_profile_id_delete(business_profile_id)

Delete Business Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BusinessProfilesApi.new
business_profile_id = 'business_profile_id_example' # String | 

begin
  # Delete Business Profile
  result = api_instance.delete_business_profile_api_v1_business_profiles_business_profile_id_delete(business_profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->delete_business_profile_api_v1_business_profiles_business_profile_id_delete: #{e}"
end
```

#### Using the delete_business_profile_api_v1_business_profiles_business_profile_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_business_profile_api_v1_business_profiles_business_profile_id_delete_with_http_info(business_profile_id)

```ruby
begin
  # Delete Business Profile
  data, status_code, headers = api_instance.delete_business_profile_api_v1_business_profiles_business_profile_id_delete_with_http_info(business_profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->delete_business_profile_api_v1_business_profiles_business_profile_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_profile_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_business_profile_api_v1_business_profiles_business_profile_id_get

> <BusinessProfileResponse> get_business_profile_api_v1_business_profiles_business_profile_id_get(business_profile_id)

Get Business Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BusinessProfilesApi.new
business_profile_id = 'business_profile_id_example' # String | 

begin
  # Get Business Profile
  result = api_instance.get_business_profile_api_v1_business_profiles_business_profile_id_get(business_profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->get_business_profile_api_v1_business_profiles_business_profile_id_get: #{e}"
end
```

#### Using the get_business_profile_api_v1_business_profiles_business_profile_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BusinessProfileResponse>, Integer, Hash)> get_business_profile_api_v1_business_profiles_business_profile_id_get_with_http_info(business_profile_id)

```ruby
begin
  # Get Business Profile
  data, status_code, headers = api_instance.get_business_profile_api_v1_business_profiles_business_profile_id_get_with_http_info(business_profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BusinessProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->get_business_profile_api_v1_business_profiles_business_profile_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_profile_id** | **String** |  |  |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_business_profiles_api_v1_business_profiles_get

> <BusinessProfilesListResponse> list_business_profiles_api_v1_business_profiles_get(opts)

List Business Profiles

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BusinessProfilesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Business Profiles
  result = api_instance.list_business_profiles_api_v1_business_profiles_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->list_business_profiles_api_v1_business_profiles_get: #{e}"
end
```

#### Using the list_business_profiles_api_v1_business_profiles_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BusinessProfilesListResponse>, Integer, Hash)> list_business_profiles_api_v1_business_profiles_get_with_http_info(opts)

```ruby
begin
  # List Business Profiles
  data, status_code, headers = api_instance.list_business_profiles_api_v1_business_profiles_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BusinessProfilesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->list_business_profiles_api_v1_business_profiles_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**BusinessProfilesListResponse**](BusinessProfilesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_business_profile_api_v1_business_profiles_business_profile_id_patch

> <BusinessProfileResponse> patch_business_profile_api_v1_business_profiles_business_profile_id_patch(business_profile_id, business_profile_patch, opts)

Patch Business Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BusinessProfilesApi.new
business_profile_id = 'business_profile_id_example' # String | 
business_profile_patch = InvoicePDFs::BusinessProfilePatch.new # BusinessProfilePatch | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Patch Business Profile
  result = api_instance.patch_business_profile_api_v1_business_profiles_business_profile_id_patch(business_profile_id, business_profile_patch, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->patch_business_profile_api_v1_business_profiles_business_profile_id_patch: #{e}"
end
```

#### Using the patch_business_profile_api_v1_business_profiles_business_profile_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BusinessProfileResponse>, Integer, Hash)> patch_business_profile_api_v1_business_profiles_business_profile_id_patch_with_http_info(business_profile_id, business_profile_patch, opts)

```ruby
begin
  # Patch Business Profile
  data, status_code, headers = api_instance.patch_business_profile_api_v1_business_profiles_business_profile_id_patch_with_http_info(business_profile_id, business_profile_patch, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BusinessProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BusinessProfilesApi->patch_business_profile_api_v1_business_profiles_business_profile_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **business_profile_id** | **String** |  |  |
| **business_profile_patch** | [**BusinessProfilePatch**](BusinessProfilePatch.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**BusinessProfileResponse**](BusinessProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

