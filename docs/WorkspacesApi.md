# InvoicePDFs::WorkspacesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**add_workspace_member**](WorkspacesApi.md#add_workspace_member) | **POST** /api/v1/workspaces/{workspace_id}/members | Add Workspace Member |
| [**create_workspace**](WorkspacesApi.md#create_workspace) | **POST** /api/v1/workspaces | Create Workspace |
| [**delete_workspace**](WorkspacesApi.md#delete_workspace) | **DELETE** /api/v1/workspaces/{workspace_id} | Delete Workspace |
| [**get_workspace**](WorkspacesApi.md#get_workspace) | **GET** /api/v1/workspaces/{workspace_id} | Get Workspace |
| [**list_workspace_members**](WorkspacesApi.md#list_workspace_members) | **GET** /api/v1/workspaces/{workspace_id}/members | List Workspace Members |
| [**list_workspaces**](WorkspacesApi.md#list_workspaces) | **GET** /api/v1/workspaces | List Workspaces |
| [**remove_workspace_member**](WorkspacesApi.md#remove_workspace_member) | **DELETE** /api/v1/workspaces/{workspace_id}/members/{member_id} | Remove Workspace Member |
| [**update_workspace**](WorkspacesApi.md#update_workspace) | **PATCH** /api/v1/workspaces/{workspace_id} | Update Workspace |
| [**update_workspace_member**](WorkspacesApi.md#update_workspace_member) | **PATCH** /api/v1/workspaces/{workspace_id}/members/{member_id} | Update Workspace Member |


## add_workspace_member

> <WorkspaceMembersListResponse> add_workspace_member(workspace_id, workspace_member_create_request, opts)

Add Workspace Member

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
  # Add Workspace Member
  result = api_instance.add_workspace_member(workspace_id, workspace_member_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->add_workspace_member: #{e}"
end
```

#### Using the add_workspace_member_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceMembersListResponse>, Integer, Hash)> add_workspace_member_with_http_info(workspace_id, workspace_member_create_request, opts)

```ruby
begin
  # Add Workspace Member
  data, status_code, headers = api_instance.add_workspace_member_with_http_info(workspace_id, workspace_member_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceMembersListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->add_workspace_member_with_http_info: #{e}"
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


## create_workspace

> <WorkspaceResponse> create_workspace(workspace_create_request, opts)

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
  result = api_instance.create_workspace(workspace_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->create_workspace: #{e}"
end
```

#### Using the create_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceResponse>, Integer, Hash)> create_workspace_with_http_info(workspace_create_request, opts)

```ruby
begin
  # Create Workspace
  data, status_code, headers = api_instance.create_workspace_with_http_info(workspace_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->create_workspace_with_http_info: #{e}"
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


## delete_workspace

> <SimpleBoolResponse> delete_workspace(workspace_id)

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
  result = api_instance.delete_workspace(workspace_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspace: #{e}"
end
```

#### Using the delete_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_workspace_with_http_info(workspace_id)

```ruby
begin
  # Delete Workspace
  data, status_code, headers = api_instance.delete_workspace_with_http_info(workspace_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->delete_workspace_with_http_info: #{e}"
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


## get_workspace

> <WorkspaceResponse> get_workspace(workspace_id)

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
  result = api_instance.get_workspace(workspace_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace: #{e}"
end
```

#### Using the get_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceResponse>, Integer, Hash)> get_workspace_with_http_info(workspace_id)

```ruby
begin
  # Get Workspace
  data, status_code, headers = api_instance.get_workspace_with_http_info(workspace_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->get_workspace_with_http_info: #{e}"
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


## list_workspace_members

> <WorkspaceMembersListResponse> list_workspace_members(workspace_id)

List Workspace Members

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
  # List Workspace Members
  result = api_instance.list_workspace_members(workspace_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspace_members: #{e}"
end
```

#### Using the list_workspace_members_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceMembersListResponse>, Integer, Hash)> list_workspace_members_with_http_info(workspace_id)

```ruby
begin
  # List Workspace Members
  data, status_code, headers = api_instance.list_workspace_members_with_http_info(workspace_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceMembersListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspace_members_with_http_info: #{e}"
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


## list_workspaces

> <WorkspacesListResponse> list_workspaces(opts)

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
  result = api_instance.list_workspaces(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspaces: #{e}"
end
```

#### Using the list_workspaces_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspacesListResponse>, Integer, Hash)> list_workspaces_with_http_info(opts)

```ruby
begin
  # List Workspaces
  data, status_code, headers = api_instance.list_workspaces_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspacesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->list_workspaces_with_http_info: #{e}"
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


## remove_workspace_member

> <SimpleBoolResponse> remove_workspace_member(workspace_id, member_id)

Remove Workspace Member

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
  # Remove Workspace Member
  result = api_instance.remove_workspace_member(workspace_id, member_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->remove_workspace_member: #{e}"
end
```

#### Using the remove_workspace_member_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> remove_workspace_member_with_http_info(workspace_id, member_id)

```ruby
begin
  # Remove Workspace Member
  data, status_code, headers = api_instance.remove_workspace_member_with_http_info(workspace_id, member_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->remove_workspace_member_with_http_info: #{e}"
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


## update_workspace

> <WorkspaceResponse> update_workspace(workspace_id, workspace_patch_request, opts)

Update Workspace

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
  # Update Workspace
  result = api_instance.update_workspace(workspace_id, workspace_patch_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace: #{e}"
end
```

#### Using the update_workspace_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceResponse>, Integer, Hash)> update_workspace_with_http_info(workspace_id, workspace_patch_request, opts)

```ruby
begin
  # Update Workspace
  data, status_code, headers = api_instance.update_workspace_with_http_info(workspace_id, workspace_patch_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace_with_http_info: #{e}"
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


## update_workspace_member

> <WorkspaceMemberOut> update_workspace_member(workspace_id, member_id, workspace_member_patch_request)

Update Workspace Member

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
  # Update Workspace Member
  result = api_instance.update_workspace_member(workspace_id, member_id, workspace_member_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace_member: #{e}"
end
```

#### Using the update_workspace_member_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WorkspaceMemberOut>, Integer, Hash)> update_workspace_member_with_http_info(workspace_id, member_id, workspace_member_patch_request)

```ruby
begin
  # Update Workspace Member
  data, status_code, headers = api_instance.update_workspace_member_with_http_info(workspace_id, member_id, workspace_member_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WorkspaceMemberOut>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WorkspacesApi->update_workspace_member_with_http_info: #{e}"
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

