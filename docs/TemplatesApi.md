# InvoicePDFs::TemplatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_template**](TemplatesApi.md#create_template) | **POST** /api/v1/templates/custom | Create Template |
| [**delete_template**](TemplatesApi.md#delete_template) | **DELETE** /api/v1/templates/custom/{template_id} | Delete Template |
| [**duplicate_template**](TemplatesApi.md#duplicate_template) | **POST** /api/v1/templates/custom/{template_id}/duplicate | Duplicate Template |
| [**get_builtin_template**](TemplatesApi.md#get_builtin_template) | **GET** /api/v1/templates/builtin/{template_id} | Get Builtin Template |
| [**get_custom_template**](TemplatesApi.md#get_custom_template) | **GET** /api/v1/templates/custom/{template_id} | Get Custom Template |
| [**get_template**](TemplatesApi.md#get_template) | **GET** /api/v1/templates/{template_id} | Get Template |
| [**list_custom_templates**](TemplatesApi.md#list_custom_templates) | **GET** /api/v1/templates/custom | List Custom Templates |
| [**list_templates**](TemplatesApi.md#list_templates) | **GET** /api/v1/templates | List Templates |
| [**preview_template**](TemplatesApi.md#preview_template) | **POST** /api/v1/templates/{template_id}/preview | Preview Template |
| [**publish_template**](TemplatesApi.md#publish_template) | **POST** /api/v1/templates/custom/{template_id}/publish | Publish Template |
| [**update_template**](TemplatesApi.md#update_template) | **PATCH** /api/v1/templates/custom/{template_id} | Update Template |


## create_template

> <CustomTemplateResponse> create_template(template_create_request)

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
  result = api_instance.create_template(template_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->create_template: #{e}"
end
```

#### Using the create_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> create_template_with_http_info(template_create_request)

```ruby
begin
  # Create Template
  data, status_code, headers = api_instance.create_template_with_http_info(template_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->create_template_with_http_info: #{e}"
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


## delete_template

> delete_template(template_id)

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
  api_instance.delete_template(template_id)
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->delete_template: #{e}"
end
```

#### Using the delete_template_with_http_info variant

This returns an Array which contains the response data (`nil` in this case), status code and headers.

> <Array(nil, Integer, Hash)> delete_template_with_http_info(template_id)

```ruby
begin
  # Delete Template
  data, status_code, headers = api_instance.delete_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => nil
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->delete_template_with_http_info: #{e}"
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


## duplicate_template

> <CustomTemplateResponse> duplicate_template(template_id)

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
  result = api_instance.duplicate_template(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->duplicate_template: #{e}"
end
```

#### Using the duplicate_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> duplicate_template_with_http_info(template_id)

```ruby
begin
  # Duplicate Template
  data, status_code, headers = api_instance.duplicate_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->duplicate_template_with_http_info: #{e}"
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


## get_builtin_template

> <TemplateDetailResponse> get_builtin_template(template_id)

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
  result = api_instance.get_builtin_template(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_builtin_template: #{e}"
end
```

#### Using the get_builtin_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplateDetailResponse>, Integer, Hash)> get_builtin_template_with_http_info(template_id)

```ruby
begin
  # Get Builtin Template
  data, status_code, headers = api_instance.get_builtin_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplateDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_builtin_template_with_http_info: #{e}"
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


## get_custom_template

> <CustomTemplateResponse> get_custom_template(template_id)

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
  result = api_instance.get_custom_template(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_custom_template: #{e}"
end
```

#### Using the get_custom_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> get_custom_template_with_http_info(template_id)

```ruby
begin
  # Get Custom Template
  data, status_code, headers = api_instance.get_custom_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_custom_template_with_http_info: #{e}"
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


## get_template

> <TemplateDetailResponse> get_template(template_id)

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
  result = api_instance.get_template(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_template: #{e}"
end
```

#### Using the get_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplateDetailResponse>, Integer, Hash)> get_template_with_http_info(template_id)

```ruby
begin
  # Get Template
  data, status_code, headers = api_instance.get_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplateDetailResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->get_template_with_http_info: #{e}"
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


## list_custom_templates

> <CustomTemplatesListResponse> list_custom_templates(opts)

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
  result = api_instance.list_custom_templates(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->list_custom_templates: #{e}"
end
```

#### Using the list_custom_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplatesListResponse>, Integer, Hash)> list_custom_templates_with_http_info(opts)

```ruby
begin
  # List Custom Templates
  data, status_code, headers = api_instance.list_custom_templates_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplatesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->list_custom_templates_with_http_info: #{e}"
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


## list_templates

> <TemplatesListResponse> list_templates

List Templates

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
  # List Templates
  result = api_instance.list_templates
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->list_templates: #{e}"
end
```

#### Using the list_templates_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TemplatesListResponse>, Integer, Hash)> list_templates_with_http_info

```ruby
begin
  # List Templates
  data, status_code, headers = api_instance.list_templates_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TemplatesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->list_templates_with_http_info: #{e}"
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


## preview_template

> <RenderResponse> preview_template(template_id, document_render_request, opts)

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
document_render_request = InvoicePDFs::DocumentRenderRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}), template: InvoicePDFs::DocumentTemplateRef.new({id: 'id_example'})}) # DocumentRenderRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Preview Template
  result = api_instance.preview_template(template_id, document_render_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->preview_template: #{e}"
end
```

#### Using the preview_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RenderResponse>, Integer, Hash)> preview_template_with_http_info(template_id, document_render_request, opts)

```ruby
begin
  # Preview Template
  data, status_code, headers = api_instance.preview_template_with_http_info(template_id, document_render_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RenderResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->preview_template_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **template_id** | **String** |  |  |
| **document_render_request** | [**DocumentRenderRequest**](DocumentRenderRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**RenderResponse**](RenderResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json, application/pdf


## publish_template

> <CustomTemplateResponse> publish_template(template_id)

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
  result = api_instance.publish_template(template_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->publish_template: #{e}"
end
```

#### Using the publish_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> publish_template_with_http_info(template_id)

```ruby
begin
  # Publish Template
  data, status_code, headers = api_instance.publish_template_with_http_info(template_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->publish_template_with_http_info: #{e}"
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


## update_template

> <CustomTemplateResponse> update_template(template_id, template_patch_request)

Update Template

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
  # Update Template
  result = api_instance.update_template(template_id, template_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->update_template: #{e}"
end
```

#### Using the update_template_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomTemplateResponse>, Integer, Hash)> update_template_with_http_info(template_id, template_patch_request)

```ruby
begin
  # Update Template
  data, status_code, headers = api_instance.update_template_with_http_info(template_id, template_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomTemplateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TemplatesApi->update_template_with_http_info: #{e}"
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

