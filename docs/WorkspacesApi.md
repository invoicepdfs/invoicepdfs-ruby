# InvoicePDFs::WorkspacesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_member_api_v1_workspaces_workspace_id_members_post**](WorkspacesApi.md#create_member_api_v1_workspaces_workspace_id_members_post) | **POST** /api/v1/workspaces/{workspace_id}/members | Create Member |
| [**create_workspace_api_v1_workspaces_post**](WorkspacesApi.md#create_workspace_api_v1_workspaces_post) | **POST** /api/v1/workspaces | Create Workspace |
| [**delete_member_api_v1_workspaces_workspace_id_members_member_id_delete**](WorkspacesApi.md#delete_member_api_v1_workspaces_workspace_id_members_member_id_delete) | **DELETE** /api/v1/workspaces/{workspace_id}/members/{member_id} | Delete Member |
| [**delete_workspace_api_v1_workspaces_workspace_id_delete**](WorkspacesApi.md#delete_workspace_api_v1_workspaces_workspace_id_delete) | **DELETE** /api/v1/workspaces/{workspace_id} | Delete Workspace |
| [**get_workspace_api_v1_workspaces_workspace_id_get**](WorkspacesApi.md#get_workspace_api_v1_workspaces_workspace_id_get) | **GET** /api/v1/workspaces/{workspace_id} | Get Workspace |
| [**list_members_api_v1_workspaces_workspace_id_members_get**](WorkspacesApi.md#list_members_api_v1_workspaces_workspace_id_members_get) | **GET** /api/v1/workspaces/{workspace_id}/members | List Members |
| [**list_workspaces_api_v1_workspaces_get**](WorkspacesApi.md#list_workspaces_api_v1_workspaces_get) | **GET** /api/v1/workspaces | List Workspaces |
| [**patch_member_api_v1_workspaces_workspace_id_members_member_id_patch**](WorkspacesApi.md#patch_member_api_v1_workspaces_workspace_id_members_member_id_patch) | **PATCH** /api/v1/workspaces/{workspace_id}/members/{member_id} | Patch Member |
| [**patch_workspace_api_v1_workspaces_workspace_id_patch**](WorkspacesApi.md#patch_workspace_api_v1_workspaces_workspace_id_patch) | **PATCH** /api/v1/workspaces/{workspace_id} | Patch Workspace |


## create_member_api_v1_workspaces_workspace_id_members_post

> <WorkspaceMembersListResponse> create_member_api_v1_workspaces_workspace_id_members_post(workspace_id, workspace_member_create_request, opts)

Create Member

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_id = 'workspace_id_example' # String | 
workspace_member_create_request = InvoicePDFs::WorkspaceMemberCreateRequest.new({email: 'teammate@acme.com'}) # WorkspaceMemberCreateRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Create Member
  result = api_instance.create_member_api_v1_workspaces_workspace_id_members_post(workspace_id, workspace_member_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->create_member_api_v1_workspaces_workspace_id_members_post: #{e}"
end
```

#### Using the create_member_api_v1_workspaces_workspace_id_members_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceMembersListResponse>, Integer, Hash)> create_member_api_v1_workspaces_workspace_id_members_post_with_http_info(workspace_id, workspace_member_create_request, opts)

```ruby
begin
  # Create Member
  data, status_code, headers = api_instance.create_member_api_v1_workspaces_workspace_id_members_post_with_http_info(workspace_id, workspace_member_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceMembersListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->create_member_api_v1_workspaces_workspace_id_members_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_id** | **String** |  |  |
| **workspace_member_create_request** | [**WorkspaceMemberCreateRequest**](WorkspaceMemberCreateRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**WorkspaceMembersListResponse**](WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_workspace_api_v1_workspaces_post

> <WorkspaceResponse> create_workspace_api_v1_workspaces_post(workspace_create_request, opts)

Create Workspace

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_create_request = InvoicePDFs::WorkspaceCreateRequest.new({name: 'Engineering Team'}) # WorkspaceCreateRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Create Workspace
  result = api_instance.create_workspace_api_v1_workspaces_post(workspace_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->create_workspace_api_v1_workspaces_post: #{e}"
end
```

#### Using the create_workspace_api_v1_workspaces_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceResponse>, Integer, Hash)> create_workspace_api_v1_workspaces_post_with_http_info(workspace_create_request, opts)

```ruby
begin
  # Create Workspace
  data, status_code, headers = api_instance.create_workspace_api_v1_workspaces_post_with_http_info(workspace_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->create_workspace_api_v1_workspaces_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_create_request** | [**WorkspaceCreateRequest**](WorkspaceCreateRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_member_api_v1_workspaces_workspace_id_members_member_id_delete

> <SimpleBoolResponse> delete_member_api_v1_workspaces_workspace_id_members_member_id_delete(workspace_id, member_id)

Delete Member

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_id = 'workspace_id_example' # String | 
member_id = 'member_id_example' # String | 

begin
  # Delete Member
  result = api_instance.delete_member_api_v1_workspaces_workspace_id_members_member_id_delete(workspace_id, member_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->delete_member_api_v1_workspaces_workspace_id_members_member_id_delete: #{e}"
end
```

#### Using the delete_member_api_v1_workspaces_workspace_id_members_member_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_member_api_v1_workspaces_workspace_id_members_member_id_delete_with_http_info(workspace_id, member_id)

```ruby
begin
  # Delete Member
  data, status_code, headers = api_instance.delete_member_api_v1_workspaces_workspace_id_members_member_id_delete_with_http_info(workspace_id, member_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->delete_member_api_v1_workspaces_workspace_id_members_member_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_id** | **String** |  |  |
| **member_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## delete_workspace_api_v1_workspaces_workspace_id_delete

> <SimpleBoolResponse> delete_workspace_api_v1_workspaces_workspace_id_delete(workspace_id)

Delete Workspace

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_id = 'workspace_id_example' # String | 

begin
  # Delete Workspace
  result = api_instance.delete_workspace_api_v1_workspaces_workspace_id_delete(workspace_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspace_api_v1_workspaces_workspace_id_delete: #{e}"
end
```

#### Using the delete_workspace_api_v1_workspaces_workspace_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_workspace_api_v1_workspaces_workspace_id_delete_with_http_info(workspace_id)

```ruby
begin
  # Delete Workspace
  data, status_code, headers = api_instance.delete_workspace_api_v1_workspaces_workspace_id_delete_with_http_info(workspace_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspace_api_v1_workspaces_workspace_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_workspace_api_v1_workspaces_workspace_id_get

> <WorkspaceResponse> get_workspace_api_v1_workspaces_workspace_id_get(workspace_id)

Get Workspace

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_id = 'workspace_id_example' # String | 

begin
  # Get Workspace
  result = api_instance.get_workspace_api_v1_workspaces_workspace_id_get(workspace_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace_api_v1_workspaces_workspace_id_get: #{e}"
end
```

#### Using the get_workspace_api_v1_workspaces_workspace_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceResponse>, Integer, Hash)> get_workspace_api_v1_workspaces_workspace_id_get_with_http_info(workspace_id)

```ruby
begin
  # Get Workspace
  data, status_code, headers = api_instance.get_workspace_api_v1_workspaces_workspace_id_get_with_http_info(workspace_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace_api_v1_workspaces_workspace_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_id** | **String** |  |  |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_members_api_v1_workspaces_workspace_id_members_get

> <WorkspaceMembersListResponse> list_members_api_v1_workspaces_workspace_id_members_get(workspace_id)

List Members

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_id = 'workspace_id_example' # String | 

begin
  # List Members
  result = api_instance.list_members_api_v1_workspaces_workspace_id_members_get(workspace_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_members_api_v1_workspaces_workspace_id_members_get: #{e}"
end
```

#### Using the list_members_api_v1_workspaces_workspace_id_members_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceMembersListResponse>, Integer, Hash)> list_members_api_v1_workspaces_workspace_id_members_get_with_http_info(workspace_id)

```ruby
begin
  # List Members
  data, status_code, headers = api_instance.list_members_api_v1_workspaces_workspace_id_members_get_with_http_info(workspace_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceMembersListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_members_api_v1_workspaces_workspace_id_members_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_id** | **String** |  |  |

### Return type

[**WorkspaceMembersListResponse**](WorkspaceMembersListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_workspaces_api_v1_workspaces_get

> <WorkspacesListResponse> list_workspaces_api_v1_workspaces_get(opts)

List Workspaces

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Workspaces
  result = api_instance.list_workspaces_api_v1_workspaces_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspaces_api_v1_workspaces_get: #{e}"
end
```

#### Using the list_workspaces_api_v1_workspaces_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspacesListResponse>, Integer, Hash)> list_workspaces_api_v1_workspaces_get_with_http_info(opts)

```ruby
begin
  # List Workspaces
  data, status_code, headers = api_instance.list_workspaces_api_v1_workspaces_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspacesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspaces_api_v1_workspaces_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**WorkspacesListResponse**](WorkspacesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_member_api_v1_workspaces_workspace_id_members_member_id_patch

> <WorkspaceMemberOut> patch_member_api_v1_workspaces_workspace_id_members_member_id_patch(workspace_id, member_id, workspace_member_patch_request)

Patch Member

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_id = 'workspace_id_example' # String | 
member_id = 'member_id_example' # String | 
workspace_member_patch_request = InvoicePDFs::WorkspaceMemberPatchRequest.new # WorkspaceMemberPatchRequest | 

begin
  # Patch Member
  result = api_instance.patch_member_api_v1_workspaces_workspace_id_members_member_id_patch(workspace_id, member_id, workspace_member_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->patch_member_api_v1_workspaces_workspace_id_members_member_id_patch: #{e}"
end
```

#### Using the patch_member_api_v1_workspaces_workspace_id_members_member_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceMemberOut>, Integer, Hash)> patch_member_api_v1_workspaces_workspace_id_members_member_id_patch_with_http_info(workspace_id, member_id, workspace_member_patch_request)

```ruby
begin
  # Patch Member
  data, status_code, headers = api_instance.patch_member_api_v1_workspaces_workspace_id_members_member_id_patch_with_http_info(workspace_id, member_id, workspace_member_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceMemberOut>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->patch_member_api_v1_workspaces_workspace_id_members_member_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_id** | **String** |  |  |
| **member_id** | **String** |  |  |
| **workspace_member_patch_request** | [**WorkspaceMemberPatchRequest**](WorkspaceMemberPatchRequest.md) |  |  |

### Return type

[**WorkspaceMemberOut**](WorkspaceMemberOut.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## patch_workspace_api_v1_workspaces_workspace_id_patch

> <WorkspaceResponse> patch_workspace_api_v1_workspaces_workspace_id_patch(workspace_id, workspace_patch_request, opts)

Patch Workspace

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WorkspacesApi.new
workspace_id = 'workspace_id_example' # String | 
workspace_patch_request = InvoicePDFs::WorkspacePatchRequest.new # WorkspacePatchRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Patch Workspace
  result = api_instance.patch_workspace_api_v1_workspaces_workspace_id_patch(workspace_id, workspace_patch_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->patch_workspace_api_v1_workspaces_workspace_id_patch: #{e}"
end
```

#### Using the patch_workspace_api_v1_workspaces_workspace_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceResponse>, Integer, Hash)> patch_workspace_api_v1_workspaces_workspace_id_patch_with_http_info(workspace_id, workspace_patch_request, opts)

```ruby
begin
  # Patch Workspace
  data, status_code, headers = api_instance.patch_workspace_api_v1_workspaces_workspace_id_patch_with_http_info(workspace_id, workspace_patch_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->patch_workspace_api_v1_workspaces_workspace_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **workspace_id** | **String** |  |  |
| **workspace_patch_request** | [**WorkspacePatchRequest**](WorkspacePatchRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**WorkspaceResponse**](WorkspaceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

