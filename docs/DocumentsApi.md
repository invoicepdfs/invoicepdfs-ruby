# InvoicePDFs::DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**calculate_document_api_v1_documents_calculate_post**](DocumentsApi.md#calculate_document_api_v1_documents_calculate_post) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**render_document_api_v1_documents_render_post**](DocumentsApi.md#render_document_api_v1_documents_render_post) | **POST** /api/v1/documents/render | Render Document |
| [**validate_document_api_v1_documents_validate_post**](DocumentsApi.md#validate_document_api_v1_documents_validate_post) | **POST** /api/v1/documents/validate | Validate Document |


## calculate_document_api_v1_documents_calculate_post

> <DocumentCalculateResponse> calculate_document_api_v1_documents_calculate_post(document_calculate_request)

Calculate Document

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DocumentsApi.new
document_calculate_request = InvoicePDFs::DocumentCalculateRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]})}) # DocumentCalculateRequest | 

begin
  # Calculate Document
  result = api_instance.calculate_document_api_v1_documents_calculate_post(document_calculate_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->calculate_document_api_v1_documents_calculate_post: #{e}"
end
```

#### Using the calculate_document_api_v1_documents_calculate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentCalculateResponse>, Integer, Hash)> calculate_document_api_v1_documents_calculate_post_with_http_info(document_calculate_request)

```ruby
begin
  # Calculate Document
  data, status_code, headers = api_instance.calculate_document_api_v1_documents_calculate_post_with_http_info(document_calculate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentCalculateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->calculate_document_api_v1_documents_calculate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_calculate_request** | [**DocumentCalculateRequest**](DocumentCalculateRequest.md) |  |  |

### Return type

[**DocumentCalculateResponse**](DocumentCalculateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## render_document_api_v1_documents_render_post

> Object render_document_api_v1_documents_render_post(document_render_request, opts)

Render Document

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DocumentsApi.new
document_render_request = InvoicePDFs::DocumentRenderRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}), template: InvoicePDFs::DocumentTemplateRef.new({id: 'id_example'})}) # DocumentRenderRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Render Document
  result = api_instance.render_document_api_v1_documents_render_post(document_render_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->render_document_api_v1_documents_render_post: #{e}"
end
```

#### Using the render_document_api_v1_documents_render_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> render_document_api_v1_documents_render_post_with_http_info(document_render_request, opts)

```ruby
begin
  # Render Document
  data, status_code, headers = api_instance.render_document_api_v1_documents_render_post_with_http_info(document_render_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->render_document_api_v1_documents_render_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_render_request** | [**DocumentRenderRequest**](DocumentRenderRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## validate_document_api_v1_documents_validate_post

> <DocumentValidateResponse> validate_document_api_v1_documents_validate_post(document_validate_request)

Validate Document

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DocumentsApi.new
document_validate_request = InvoicePDFs::DocumentValidateRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]})}) # DocumentValidateRequest | 

begin
  # Validate Document
  result = api_instance.validate_document_api_v1_documents_validate_post(document_validate_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->validate_document_api_v1_documents_validate_post: #{e}"
end
```

#### Using the validate_document_api_v1_documents_validate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentValidateResponse>, Integer, Hash)> validate_document_api_v1_documents_validate_post_with_http_info(document_validate_request)

```ruby
begin
  # Validate Document
  data, status_code, headers = api_instance.validate_document_api_v1_documents_validate_post_with_http_info(document_validate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentValidateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->validate_document_api_v1_documents_validate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_validate_request** | [**DocumentValidateRequest**](DocumentValidateRequest.md) |  |  |

### Return type

[**DocumentValidateResponse**](DocumentValidateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

