# InvoicePDFs::BrandingProfilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_branding_profile**](BrandingProfilesApi.md#create_branding_profile) | **POST** /api/v1/branding-profiles | Create Branding Profile |
| [**delete_branding_logo**](BrandingProfilesApi.md#delete_branding_logo) | **DELETE** /api/v1/branding-profiles/{profile_id}/logo | Delete Branding Logo |
| [**delete_branding_profile**](BrandingProfilesApi.md#delete_branding_profile) | **DELETE** /api/v1/branding-profiles/{profile_id} | Delete Branding Profile |
| [**get_branding_profile**](BrandingProfilesApi.md#get_branding_profile) | **GET** /api/v1/branding-profiles/{profile_id} | Get Branding Profile |
| [**list_branding_profiles**](BrandingProfilesApi.md#list_branding_profiles) | **GET** /api/v1/branding-profiles | List Branding Profiles |
| [**set_default_branding_profile**](BrandingProfilesApi.md#set_default_branding_profile) | **POST** /api/v1/branding-profiles/{profile_id}/default | Set Default Branding Profile |
| [**update_branding_profile**](BrandingProfilesApi.md#update_branding_profile) | **PATCH** /api/v1/branding-profiles/{profile_id} | Update Branding Profile |
| [**upload_branding_logo**](BrandingProfilesApi.md#upload_branding_logo) | **POST** /api/v1/branding-profiles/{profile_id}/logo | Upload Branding Logo |


## create_branding_profile

> <BrandingProfileResponse> create_branding_profile(branding_profile_create_request)

Create Branding Profile

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
  # Create Branding Profile
  result = api_instance.create_branding_profile(branding_profile_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->create_branding_profile: #{e}"
end
```

#### Using the create_branding_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> create_branding_profile_with_http_info(branding_profile_create_request)

```ruby
begin
  # Create Branding Profile
  data, status_code, headers = api_instance.create_branding_profile_with_http_info(branding_profile_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->create_branding_profile_with_http_info: #{e}"
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


## delete_branding_logo

> <SimpleBoolResponse> delete_branding_logo(profile_id)

Delete Branding Logo

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
  # Delete Branding Logo
  result = api_instance.delete_branding_logo(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_branding_logo: #{e}"
end
```

#### Using the delete_branding_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_branding_logo_with_http_info(profile_id)

```ruby
begin
  # Delete Branding Logo
  data, status_code, headers = api_instance.delete_branding_logo_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_branding_logo_with_http_info: #{e}"
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


## delete_branding_profile

> <SimpleBoolResponse> delete_branding_profile(profile_id)

Delete Branding Profile

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
  # Delete Branding Profile
  result = api_instance.delete_branding_profile(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_branding_profile: #{e}"
end
```

#### Using the delete_branding_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_branding_profile_with_http_info(profile_id)

```ruby
begin
  # Delete Branding Profile
  data, status_code, headers = api_instance.delete_branding_profile_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->delete_branding_profile_with_http_info: #{e}"
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


## get_branding_profile

> <BrandingProfileResponse> get_branding_profile(profile_id)

Get Branding Profile

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
  # Get Branding Profile
  result = api_instance.get_branding_profile(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->get_branding_profile: #{e}"
end
```

#### Using the get_branding_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> get_branding_profile_with_http_info(profile_id)

```ruby
begin
  # Get Branding Profile
  data, status_code, headers = api_instance.get_branding_profile_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->get_branding_profile_with_http_info: #{e}"
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


## list_branding_profiles

> <BrandingProfilesListResponse> list_branding_profiles

List Branding Profiles

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
  # List Branding Profiles
  result = api_instance.list_branding_profiles
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->list_branding_profiles: #{e}"
end
```

#### Using the list_branding_profiles_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfilesListResponse>, Integer, Hash)> list_branding_profiles_with_http_info

```ruby
begin
  # List Branding Profiles
  data, status_code, headers = api_instance.list_branding_profiles_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfilesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->list_branding_profiles_with_http_info: #{e}"
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


## set_default_branding_profile

> <BrandingProfileResponse> set_default_branding_profile(profile_id)

Set Default Branding Profile

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
  # Set Default Branding Profile
  result = api_instance.set_default_branding_profile(profile_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->set_default_branding_profile: #{e}"
end
```

#### Using the set_default_branding_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> set_default_branding_profile_with_http_info(profile_id)

```ruby
begin
  # Set Default Branding Profile
  data, status_code, headers = api_instance.set_default_branding_profile_with_http_info(profile_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->set_default_branding_profile_with_http_info: #{e}"
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


## update_branding_profile

> <BrandingProfileResponse> update_branding_profile(profile_id, branding_profile_patch_request)

Update Branding Profile

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
  # Update Branding Profile
  result = api_instance.update_branding_profile(profile_id, branding_profile_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->update_branding_profile: #{e}"
end
```

#### Using the update_branding_profile_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> update_branding_profile_with_http_info(profile_id, branding_profile_patch_request)

```ruby
begin
  # Update Branding Profile
  data, status_code, headers = api_instance.update_branding_profile_with_http_info(profile_id, branding_profile_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->update_branding_profile_with_http_info: #{e}"
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


## upload_branding_logo

> <BrandingProfileResponse> upload_branding_logo(profile_id, file)

Upload Branding Logo

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
  # Upload Branding Logo
  result = api_instance.upload_branding_logo(profile_id, file)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->upload_branding_logo: #{e}"
end
```

#### Using the upload_branding_logo_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BrandingProfileResponse>, Integer, Hash)> upload_branding_logo_with_http_info(profile_id, file)

```ruby
begin
  # Upload Branding Logo
  data, status_code, headers = api_instance.upload_branding_logo_with_http_info(profile_id, file)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BrandingProfileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BrandingProfilesApi->upload_branding_logo_with_http_info: #{e}"
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

