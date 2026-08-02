# InvoicePDFs::BrandingProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_profile_api_v1_branding_profiles_post**](BrandingProfilesApi.md#create_profile_api_v1_branding_profiles_post) | **POST** /api/v1/branding-profiles | Create Profile |
| [**delete_logo_api_v1_branding_profiles_profile_id_logo_delete**](BrandingProfilesApi.md#delete_logo_api_v1_branding_profiles_profile_id_logo_delete) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Logo |
| [**delete_profile_api_v1_branding_profiles_profile_id_delete**](BrandingProfilesApi.md#delete_profile_api_v1_branding_profiles_profile_id_delete) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Profile |
| [**get_profile_api_v1_branding_profiles_profile_id_get**](BrandingProfilesApi.md#get_profile_api_v1_branding_profiles_profile_id_get) | **GET** /api/v1/branding-profiles/{profile_id} | Get Profile |
| [**list_profiles_api_v1_branding_profiles_get**](BrandingProfilesApi.md#list_profiles_api_v1_branding_profiles_get) | **GET** /api/v1/branding-profiles | List Profiles |
| [**set_default_api_v1_branding_profiles_profile_id_default_post**](BrandingProfilesApi.md#set_default_api_v1_branding_profiles_profile_id_default_post) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default |
| [**update_profile_api_v1_branding_profiles_profile_id_patch**](BrandingProfilesApi.md#update_profile_api_v1_branding_profiles_profile_id_patch) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Profile |
| [**upload_logo_api_v1_branding_profiles_profile_id_logo_post**](BrandingProfilesApi.md#upload_logo_api_v1_branding_profiles_profile_id_logo_post) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Logo |


## create_profile_api_v1_branding_profiles_post

> <BrandingProfileResponse> create_profile_api_v1_branding_profiles_post(branding_profile_create_request)

Create Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingProfilesApi.new
branding_profile_create_request = InvoicePDFs::BrandingProfileCreateRequest.new({name: 'Acme Corp'}) # BrandingProfileCreateRequest | 

begin
  # Create Profile
  result = api_instance.create_profile_api_v1_branding_profiles_post(branding_profile_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->create_profile_api_v1_branding_profiles_post: #{e}"
end
```

#### Using the create_profile_api_v1_branding_profiles_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> create_profile_api_v1_branding_profiles_post_with_http_info(branding_profile_create_request)

```ruby
begin
  # Create Profile
  data, status_code, headers = api_instance.create_profile_api_v1_branding_profiles_post_with_http_info(branding_profile_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->create_profile_api_v1_branding_profiles_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **branding_profile_create_request** | [**BrandingProfileCreateRequest**](BrandingProfileCreateRequest.md) |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_logo_api_v1_branding_profiles_profile_id_logo_delete

> <SimpleBoolResponse> delete_logo_api_v1_branding_profiles_profile_id_logo_delete(profile_id)

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

api_instance = InvoicePDFs::BrandingProfilesApi.new
profile_id = 'profile_id_example' # String | 

begin
  # Delete Logo
  result = api_instance.delete_logo_api_v1_branding_profiles_profile_id_logo_delete(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_logo_api_v1_branding_profiles_profile_id_logo_delete: #{e}"
end
```

#### Using the delete_logo_api_v1_branding_profiles_profile_id_logo_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_logo_api_v1_branding_profiles_profile_id_logo_delete_with_http_info(profile_id)

```ruby
begin
  # Delete Logo
  data, status_code, headers = api_instance.delete_logo_api_v1_branding_profiles_profile_id_logo_delete_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_logo_api_v1_branding_profiles_profile_id_logo_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_profile_api_v1_branding_profiles_profile_id_delete

> <SimpleBoolResponse> delete_profile_api_v1_branding_profiles_profile_id_delete(profile_id)

Delete Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingProfilesApi.new
profile_id = 'profile_id_example' # String | 

begin
  # Delete Profile
  result = api_instance.delete_profile_api_v1_branding_profiles_profile_id_delete(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_profile_api_v1_branding_profiles_profile_id_delete: #{e}"
end
```

#### Using the delete_profile_api_v1_branding_profiles_profile_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_profile_api_v1_branding_profiles_profile_id_delete_with_http_info(profile_id)

```ruby
begin
  # Delete Profile
  data, status_code, headers = api_instance.delete_profile_api_v1_branding_profiles_profile_id_delete_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_profile_api_v1_branding_profiles_profile_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_profile_api_v1_branding_profiles_profile_id_get

> <BrandingProfileResponse> get_profile_api_v1_branding_profiles_profile_id_get(profile_id)

Get Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingProfilesApi.new
profile_id = 'profile_id_example' # String | 

begin
  # Get Profile
  result = api_instance.get_profile_api_v1_branding_profiles_profile_id_get(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->get_profile_api_v1_branding_profiles_profile_id_get: #{e}"
end
```

#### Using the get_profile_api_v1_branding_profiles_profile_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> get_profile_api_v1_branding_profiles_profile_id_get_with_http_info(profile_id)

```ruby
begin
  # Get Profile
  data, status_code, headers = api_instance.get_profile_api_v1_branding_profiles_profile_id_get_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->get_profile_api_v1_branding_profiles_profile_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_profiles_api_v1_branding_profiles_get

> <BrandingProfilesListResponse> list_profiles_api_v1_branding_profiles_get

List Profiles

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingProfilesApi.new

begin
  # List Profiles
  result = api_instance.list_profiles_api_v1_branding_profiles_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->list_profiles_api_v1_branding_profiles_get: #{e}"
end
```

#### Using the list_profiles_api_v1_branding_profiles_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfilesListResponse>, Integer, Hash)> list_profiles_api_v1_branding_profiles_get_with_http_info

```ruby
begin
  # List Profiles
  data, status_code, headers = api_instance.list_profiles_api_v1_branding_profiles_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfilesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->list_profiles_api_v1_branding_profiles_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BrandingProfilesListResponse**](BrandingProfilesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## set_default_api_v1_branding_profiles_profile_id_default_post

> <BrandingProfileResponse> set_default_api_v1_branding_profiles_profile_id_default_post(profile_id)

Set Default

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingProfilesApi.new
profile_id = 'profile_id_example' # String | 

begin
  # Set Default
  result = api_instance.set_default_api_v1_branding_profiles_profile_id_default_post(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->set_default_api_v1_branding_profiles_profile_id_default_post: #{e}"
end
```

#### Using the set_default_api_v1_branding_profiles_profile_id_default_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> set_default_api_v1_branding_profiles_profile_id_default_post_with_http_info(profile_id)

```ruby
begin
  # Set Default
  data, status_code, headers = api_instance.set_default_api_v1_branding_profiles_profile_id_default_post_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->set_default_api_v1_branding_profiles_profile_id_default_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_profile_api_v1_branding_profiles_profile_id_patch

> <BrandingProfileResponse> update_profile_api_v1_branding_profiles_profile_id_patch(profile_id, branding_profile_patch_request)

Update Profile

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BrandingProfilesApi.new
profile_id = 'profile_id_example' # String | 
branding_profile_patch_request = InvoicePDFs::BrandingProfilePatchRequest.new # BrandingProfilePatchRequest | 

begin
  # Update Profile
  result = api_instance.update_profile_api_v1_branding_profiles_profile_id_patch(profile_id, branding_profile_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->update_profile_api_v1_branding_profiles_profile_id_patch: #{e}"
end
```

#### Using the update_profile_api_v1_branding_profiles_profile_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> update_profile_api_v1_branding_profiles_profile_id_patch_with_http_info(profile_id, branding_profile_patch_request)

```ruby
begin
  # Update Profile
  data, status_code, headers = api_instance.update_profile_api_v1_branding_profiles_profile_id_patch_with_http_info(profile_id, branding_profile_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->update_profile_api_v1_branding_profiles_profile_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **branding_profile_patch_request** | [**BrandingProfilePatchRequest**](BrandingProfilePatchRequest.md) |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## upload_logo_api_v1_branding_profiles_profile_id_logo_post

> <BrandingProfileResponse> upload_logo_api_v1_branding_profiles_profile_id_logo_post(profile_id, file)

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

api_instance = InvoicePDFs::BrandingProfilesApi.new
profile_id = 'profile_id_example' # String | 
file = File.new('/path/to/some/file') # File | 

begin
  # Upload Logo
  result = api_instance.upload_logo_api_v1_branding_profiles_profile_id_logo_post(profile_id, file)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->upload_logo_api_v1_branding_profiles_profile_id_logo_post: #{e}"
end
```

#### Using the upload_logo_api_v1_branding_profiles_profile_id_logo_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> upload_logo_api_v1_branding_profiles_profile_id_logo_post_with_http_info(profile_id, file)

```ruby
begin
  # Upload Logo
  data, status_code, headers = api_instance.upload_logo_api_v1_branding_profiles_profile_id_logo_post_with_http_info(profile_id, file)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->upload_logo_api_v1_branding_profiles_profile_id_logo_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **profile_id** | **String** |  |  |
| **file** | **File** |  |  |

### Return type

[**BrandingProfileResponse**](BrandingProfileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

