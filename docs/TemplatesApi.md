# InvoicePDFs::TemplatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_template_api_v1_templates_custom_post**](TemplatesApi.md#create_template_api_v1_templates_custom_post) | **POST** /api/v1/templates/custom | Create Template |
| [**delete_template_api_v1_templates_custom_template_id_delete**](TemplatesApi.md#delete_template_api_v1_templates_custom_template_id_delete) | **DELETE** /api/v1/templates/custom/{template_id} | Delete Template |
| [**duplicate_template_api_v1_templates_custom_template_id_duplicate_post**](TemplatesApi.md#duplicate_template_api_v1_templates_custom_template_id_duplicate_post) | **POST** /api/v1/templates/custom/{template_id}/duplicate | Duplicate Template |
| [**get_builtin_template_api_v1_templates_builtin_template_id_get**](TemplatesApi.md#get_builtin_template_api_v1_templates_builtin_template_id_get) | **GET** /api/v1/templates/builtin/{template_id} | Get Builtin Template |
| [**get_custom_template_api_v1_templates_custom_template_id_get**](TemplatesApi.md#get_custom_template_api_v1_templates_custom_template_id_get) | **GET** /api/v1/templates/custom/{template_id} | Get Custom Template |
| [**get_template_api_v1_templates_template_id_get**](TemplatesApi.md#get_template_api_v1_templates_template_id_get) | **GET** /api/v1/templates/{template_id} | Get Template |
| [**list_custom_templates_api_v1_templates_custom_get**](TemplatesApi.md#list_custom_templates_api_v1_templates_custom_get) | **GET** /api/v1/templates/custom | List Custom Templates |
| [**patch_template_api_v1_templates_custom_template_id_patch**](TemplatesApi.md#patch_template_api_v1_templates_custom_template_id_patch) | **PATCH** /api/v1/templates/custom/{template_id} | Patch Template |
| [**preview_template_api_v1_templates_template_id_preview_post**](TemplatesApi.md#preview_template_api_v1_templates_template_id_preview_post) | **POST** /api/v1/templates/{template_id}/preview | Preview Template |
| [**publish_template_api_v1_templates_custom_template_id_publish_post**](TemplatesApi.md#publish_template_api_v1_templates_custom_template_id_publish_post) | **POST** /api/v1/templates/custom/{template_id}/publish | Publish Template |
| [**templates_api_v1_templates_get**](TemplatesApi.md#templates_api_v1_templates_get) | **GET** /api/v1/templates | Templates |


## create_template_api_v1_templates_custom_post

> <CustomTemplateResponse> create_template_api_v1_templates_custom_post(template_create_request)

Create Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_create_request = InvoicePDFs::TemplateCreateRequest.new({name: 'name_example'}) # TemplateCreateRequest | 

begin
  # Create Template
  result = api_instance.create_template_api_v1_templates_custom_post(template_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->create_template_api_v1_templates_custom_post: #{e}"
end
```

#### Using the create_template_api_v1_templates_custom_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> create_template_api_v1_templates_custom_post_with_http_info(template_create_request)

```ruby
begin
  # Create Template
  data, status_code, headers = api_instance.create_template_api_v1_templates_custom_post_with_http_info(template_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->create_template_api_v1_templates_custom_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_create_request** | [**TemplateCreateRequest**](TemplateCreateRequest.md) |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_template_api_v1_templates_custom_template_id_delete

> delete_template_api_v1_templates_custom_template_id_delete(template_id)

Delete Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 

begin
  # Delete Template
  api_instance.delete_template_api_v1_templates_custom_template_id_delete(template_id)
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->delete_template_api_v1_templates_custom_template_id_delete: #{e}"
end
```

#### Using the delete_template_api_v1_templates_custom_template_id_delete_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_template_api_v1_templates_custom_template_id_delete_with_http_info(template_id)

```ruby
begin
  # Delete Template
  data, status_code, headers = api_instance.delete_template_api_v1_templates_custom_template_id_delete_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->delete_template_api_v1_templates_custom_template_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

nil (empty response body)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duplicate_template_api_v1_templates_custom_template_id_duplicate_post

> <CustomTemplateResponse> duplicate_template_api_v1_templates_custom_template_id_duplicate_post(template_id)

Duplicate Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 

begin
  # Duplicate Template
  result = api_instance.duplicate_template_api_v1_templates_custom_template_id_duplicate_post(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->duplicate_template_api_v1_templates_custom_template_id_duplicate_post: #{e}"
end
```

#### Using the duplicate_template_api_v1_templates_custom_template_id_duplicate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> duplicate_template_api_v1_templates_custom_template_id_duplicate_post_with_http_info(template_id)

```ruby
begin
  # Duplicate Template
  data, status_code, headers = api_instance.duplicate_template_api_v1_templates_custom_template_id_duplicate_post_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->duplicate_template_api_v1_templates_custom_template_id_duplicate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_builtin_template_api_v1_templates_builtin_template_id_get

> <TemplateDetailResponse> get_builtin_template_api_v1_templates_builtin_template_id_get(template_id)

Get Builtin Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 

begin
  # Get Builtin Template
  result = api_instance.get_builtin_template_api_v1_templates_builtin_template_id_get(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_builtin_template_api_v1_templates_builtin_template_id_get: #{e}"
end
```

#### Using the get_builtin_template_api_v1_templates_builtin_template_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplateDetailResponse>, Integer, Hash)> get_builtin_template_api_v1_templates_builtin_template_id_get_with_http_info(template_id)

```ruby
begin
  # Get Builtin Template
  data, status_code, headers = api_instance.get_builtin_template_api_v1_templates_builtin_template_id_get_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplateDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_builtin_template_api_v1_templates_builtin_template_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

[**TemplateDetailResponse**](TemplateDetailResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_custom_template_api_v1_templates_custom_template_id_get

> <CustomTemplateResponse> get_custom_template_api_v1_templates_custom_template_id_get(template_id)

Get Custom Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 

begin
  # Get Custom Template
  result = api_instance.get_custom_template_api_v1_templates_custom_template_id_get(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_custom_template_api_v1_templates_custom_template_id_get: #{e}"
end
```

#### Using the get_custom_template_api_v1_templates_custom_template_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> get_custom_template_api_v1_templates_custom_template_id_get_with_http_info(template_id)

```ruby
begin
  # Get Custom Template
  data, status_code, headers = api_instance.get_custom_template_api_v1_templates_custom_template_id_get_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_custom_template_api_v1_templates_custom_template_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_template_api_v1_templates_template_id_get

> <TemplateDetailResponse> get_template_api_v1_templates_template_id_get(template_id)

Get Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 

begin
  # Get Template
  result = api_instance.get_template_api_v1_templates_template_id_get(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_template_api_v1_templates_template_id_get: #{e}"
end
```

#### Using the get_template_api_v1_templates_template_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplateDetailResponse>, Integer, Hash)> get_template_api_v1_templates_template_id_get_with_http_info(template_id)

```ruby
begin
  # Get Template
  data, status_code, headers = api_instance.get_template_api_v1_templates_template_id_get_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplateDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_template_api_v1_templates_template_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

[**TemplateDetailResponse**](TemplateDetailResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_custom_templates_api_v1_templates_custom_get

> <CustomTemplatesListResponse> list_custom_templates_api_v1_templates_custom_get(opts)

List Custom Templates

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Custom Templates
  result = api_instance.list_custom_templates_api_v1_templates_custom_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->list_custom_templates_api_v1_templates_custom_get: #{e}"
end
```

#### Using the list_custom_templates_api_v1_templates_custom_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplatesListResponse>, Integer, Hash)> list_custom_templates_api_v1_templates_custom_get_with_http_info(opts)

```ruby
begin
  # List Custom Templates
  data, status_code, headers = api_instance.list_custom_templates_api_v1_templates_custom_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplatesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->list_custom_templates_api_v1_templates_custom_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**CustomTemplatesListResponse**](CustomTemplatesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_template_api_v1_templates_custom_template_id_patch

> <CustomTemplateResponse> patch_template_api_v1_templates_custom_template_id_patch(template_id, template_patch_request)

Patch Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 
template_patch_request = InvoicePDFs::TemplatePatchRequest.new # TemplatePatchRequest | 

begin
  # Patch Template
  result = api_instance.patch_template_api_v1_templates_custom_template_id_patch(template_id, template_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->patch_template_api_v1_templates_custom_template_id_patch: #{e}"
end
```

#### Using the patch_template_api_v1_templates_custom_template_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> patch_template_api_v1_templates_custom_template_id_patch_with_http_info(template_id, template_patch_request)

```ruby
begin
  # Patch Template
  data, status_code, headers = api_instance.patch_template_api_v1_templates_custom_template_id_patch_with_http_info(template_id, template_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->patch_template_api_v1_templates_custom_template_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |
| **template_patch_request** | [**TemplatePatchRequest**](TemplatePatchRequest.md) |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## preview_template_api_v1_templates_template_id_preview_post

> Object preview_template_api_v1_templates_template_id_preview_post(template_id, app_schemas_v1_document_render_request, opts)

Preview Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 
app_schemas_v1_document_render_request = InvoicePDFs::AppSchemasV1DocumentRenderRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}), template: InvoicePDFs::DocumentTemplateRef.new({id: 'id_example'})}) # AppSchemasV1DocumentRenderRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Preview Template
  result = api_instance.preview_template_api_v1_templates_template_id_preview_post(template_id, app_schemas_v1_document_render_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->preview_template_api_v1_templates_template_id_preview_post: #{e}"
end
```

#### Using the preview_template_api_v1_templates_template_id_preview_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> preview_template_api_v1_templates_template_id_preview_post_with_http_info(template_id, app_schemas_v1_document_render_request, opts)

```ruby
begin
  # Preview Template
  data, status_code, headers = api_instance.preview_template_api_v1_templates_template_id_preview_post_with_http_info(template_id, app_schemas_v1_document_render_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->preview_template_api_v1_templates_template_id_preview_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |
| **app_schemas_v1_document_render_request** | [**AppSchemasV1DocumentRenderRequest**](AppSchemasV1DocumentRenderRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## publish_template_api_v1_templates_custom_template_id_publish_post

> <CustomTemplateResponse> publish_template_api_v1_templates_custom_template_id_publish_post(template_id)

Publish Template

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new
template_id = 'template_id_example' # String | 

begin
  # Publish Template
  result = api_instance.publish_template_api_v1_templates_custom_template_id_publish_post(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->publish_template_api_v1_templates_custom_template_id_publish_post: #{e}"
end
```

#### Using the publish_template_api_v1_templates_custom_template_id_publish_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> publish_template_api_v1_templates_custom_template_id_publish_post_with_http_info(template_id)

```ruby
begin
  # Publish Template
  data, status_code, headers = api_instance.publish_template_api_v1_templates_custom_template_id_publish_post_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->publish_template_api_v1_templates_custom_template_id_publish_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |

### Return type

[**CustomTemplateResponse**](CustomTemplateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## templates_api_v1_templates_get

> <TemplatesListResponse> templates_api_v1_templates_get

Templates

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TemplatesApi.new

begin
  # Templates
  result = api_instance.templates_api_v1_templates_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->templates_api_v1_templates_get: #{e}"
end
```

#### Using the templates_api_v1_templates_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplatesListResponse>, Integer, Hash)> templates_api_v1_templates_get_with_http_info

```ruby
begin
  # Templates
  data, status_code, headers = api_instance.templates_api_v1_templates_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplatesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->templates_api_v1_templates_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**TemplatesListResponse**](TemplatesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

