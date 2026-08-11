# InvoicePDFs::DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**archive_document**](DocumentsApi.md#archive_document) | **POST** /api/v1/documents/{document_id}/archive | Archive Document |
| [**calculate_document**](DocumentsApi.md#calculate_document) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**create_document**](DocumentsApi.md#create_document) | **POST** /api/v1/documents | Create Document |
| [**create_document_render**](DocumentsApi.md#create_document_render) | **POST** /api/v1/documents/{document_id}/renders | Create Document Render |
| [**delete_document**](DocumentsApi.md#delete_document) | **DELETE** /api/v1/documents/{document_id} | Delete Document |
| [**duplicate_document**](DocumentsApi.md#duplicate_document) | **POST** /api/v1/documents/{document_id}/duplicate | Duplicate Document |
| [**finalize_document**](DocumentsApi.md#finalize_document) | **POST** /api/v1/documents/{document_id}/finalize | Finalize Document |
| [**get_document**](DocumentsApi.md#get_document) | **GET** /api/v1/documents/{document_id} | Get Document |
| [**list_document_deliveries**](DocumentsApi.md#list_document_deliveries) | **GET** /api/v1/documents/{document_id}/deliveries | List Document Deliveries |
| [**list_documents**](DocumentsApi.md#list_documents) | **GET** /api/v1/documents | List Documents |
| [**mark_paid**](DocumentsApi.md#mark_paid) | **POST** /api/v1/documents/{document_id}/mark-paid | Mark Paid |
| [**mark_sent**](DocumentsApi.md#mark_sent) | **POST** /api/v1/documents/{document_id}/mark-sent | Mark Sent |
| [**mark_unpaid**](DocumentsApi.md#mark_unpaid) | **POST** /api/v1/documents/{document_id}/mark-unpaid | Mark Unpaid |
| [**render_document**](DocumentsApi.md#render_document) | **POST** /api/v1/documents/render | Render Document |
| [**restore_document**](DocumentsApi.md#restore_document) | **POST** /api/v1/documents/{document_id}/restore | Restore Document |
| [**send_document**](DocumentsApi.md#send_document) | **POST** /api/v1/documents/{document_id}/send | Send Document |
| [**update_document**](DocumentsApi.md#update_document) | **PATCH** /api/v1/documents/{document_id} | Update Document |
| [**validate_document**](DocumentsApi.md#validate_document) | **POST** /api/v1/documents/validate | Validate Document |
| [**void_document**](DocumentsApi.md#void_document) | **POST** /api/v1/documents/{document_id}/void | Void Document |


## archive_document

> <DocumentResponse> archive_document(document_id)

Archive Document

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
document_id = 'document_id_example' # String | 

begin
  # Archive Document
  result = api_instance.archive_document(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->archive_document: #{e}"
end
```

#### Using the archive_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> archive_document_with_http_info(document_id)

```ruby
begin
  # Archive Document
  data, status_code, headers = api_instance.archive_document_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->archive_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## calculate_document

> <DocumentCalculateResponse> calculate_document(document_calculate_request)

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
  result = api_instance.calculate_document(document_calculate_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->calculate_document: #{e}"
end
```

#### Using the calculate_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentCalculateResponse>, Integer, Hash)> calculate_document_with_http_info(document_calculate_request)

```ruby
begin
  # Calculate Document
  data, status_code, headers = api_instance.calculate_document_with_http_info(document_calculate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentCalculateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->calculate_document_with_http_info: #{e}"
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


## create_document

> <DocumentResponse> create_document(document_create_request, opts)

Create Document

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
document_create_request = InvoicePDFs::DocumentCreateRequest.new({number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', business_profile_id: 'bp_01ABC', customer_id: 'cus_01XYZ', line_items: [InvoicePDFs::StandardLineItemInput.new({name: 'Web Development', quantity: '2'})]}) # DocumentCreateRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Create Document
  result = api_instance.create_document(document_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->create_document: #{e}"
end
```

#### Using the create_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> create_document_with_http_info(document_create_request, opts)

```ruby
begin
  # Create Document
  data, status_code, headers = api_instance.create_document_with_http_info(document_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->create_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_create_request** | [**DocumentCreateRequest**](DocumentCreateRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_document_render

> Object create_document_render(document_id, document_render_options, opts)

Create Document Render

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
document_id = 'document_id_example' # String | 
document_render_options = InvoicePDFs::DocumentRenderOptions.new # DocumentRenderOptions | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Create Document Render
  result = api_instance.create_document_render(document_id, document_render_options, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->create_document_render: #{e}"
end
```

#### Using the create_document_render_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> create_document_render_with_http_info(document_id, document_render_options, opts)

```ruby
begin
  # Create Document Render
  data, status_code, headers = api_instance.create_document_render_with_http_info(document_id, document_render_options, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->create_document_render_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **document_render_options** | [**DocumentRenderOptions**](DocumentRenderOptions.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_document

> <SimpleBoolResponse> delete_document(document_id)

Delete Document

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
document_id = 'document_id_example' # String | 

begin
  # Delete Document
  result = api_instance.delete_document(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->delete_document: #{e}"
end
```

#### Using the delete_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_document_with_http_info(document_id)

```ruby
begin
  # Delete Document
  data, status_code, headers = api_instance.delete_document_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->delete_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duplicate_document

> <DocumentResponse> duplicate_document(document_id)

Duplicate Document

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
document_id = 'document_id_example' # String | 

begin
  # Duplicate Document
  result = api_instance.duplicate_document(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->duplicate_document: #{e}"
end
```

#### Using the duplicate_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> duplicate_document_with_http_info(document_id)

```ruby
begin
  # Duplicate Document
  data, status_code, headers = api_instance.duplicate_document_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->duplicate_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## finalize_document

> <DocumentResponse> finalize_document(document_id)

Finalize Document

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
document_id = 'document_id_example' # String | 

begin
  # Finalize Document
  result = api_instance.finalize_document(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->finalize_document: #{e}"
end
```

#### Using the finalize_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> finalize_document_with_http_info(document_id)

```ruby
begin
  # Finalize Document
  data, status_code, headers = api_instance.finalize_document_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->finalize_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_document

> <DocumentResponse> get_document(document_id)

Get Document

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
document_id = 'document_id_example' # String | 

begin
  # Get Document
  result = api_instance.get_document(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->get_document: #{e}"
end
```

#### Using the get_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> get_document_with_http_info(document_id)

```ruby
begin
  # Get Document
  data, status_code, headers = api_instance.get_document_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->get_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_document_deliveries

> <DeliveriesListResponse> list_document_deliveries(document_id, opts)

List Document Deliveries

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
document_id = 'document_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Document Deliveries
  result = api_instance.list_document_deliveries(document_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_document_deliveries: #{e}"
end
```

#### Using the list_document_deliveries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveriesListResponse>, Integer, Hash)> list_document_deliveries_with_http_info(document_id, opts)

```ruby
begin
  # List Document Deliveries
  data, status_code, headers = api_instance.list_document_deliveries_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveriesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_document_deliveries_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**DeliveriesListResponse**](DeliveriesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_documents

> <DocumentsListResponse> list_documents(opts)

List Documents

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
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example', # String | 
  document_type: 'document_type_example', # String | 
  status: 'status_example' # String | 
}

begin
  # List Documents
  result = api_instance.list_documents(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_documents: #{e}"
end
```

#### Using the list_documents_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentsListResponse>, Integer, Hash)> list_documents_with_http_info(opts)

```ruby
begin
  # List Documents
  data, status_code, headers = api_instance.list_documents_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_documents_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |
| **document_type** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |

### Return type

[**DocumentsListResponse**](DocumentsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## mark_paid

> <DocumentResponse> mark_paid(document_id)

Mark Paid

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
document_id = 'document_id_example' # String | 

begin
  # Mark Paid
  result = api_instance.mark_paid(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_paid: #{e}"
end
```

#### Using the mark_paid_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> mark_paid_with_http_info(document_id)

```ruby
begin
  # Mark Paid
  data, status_code, headers = api_instance.mark_paid_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_paid_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## mark_sent

> <DocumentResponse> mark_sent(document_id)

Mark Sent

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
document_id = 'document_id_example' # String | 

begin
  # Mark Sent
  result = api_instance.mark_sent(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_sent: #{e}"
end
```

#### Using the mark_sent_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> mark_sent_with_http_info(document_id)

```ruby
begin
  # Mark Sent
  data, status_code, headers = api_instance.mark_sent_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_sent_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## mark_unpaid

> <DocumentResponse> mark_unpaid(document_id)

Mark Unpaid

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
document_id = 'document_id_example' # String | 

begin
  # Mark Unpaid
  result = api_instance.mark_unpaid(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_unpaid: #{e}"
end
```

#### Using the mark_unpaid_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> mark_unpaid_with_http_info(document_id)

```ruby
begin
  # Mark Unpaid
  data, status_code, headers = api_instance.mark_unpaid_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_unpaid_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## render_document

> Object render_document(document_render_request, opts)

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
  result = api_instance.render_document(document_render_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->render_document: #{e}"
end
```

#### Using the render_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> render_document_with_http_info(document_render_request, opts)

```ruby
begin
  # Render Document
  data, status_code, headers = api_instance.render_document_with_http_info(document_render_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->render_document_with_http_info: #{e}"
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


## restore_document

> <DocumentResponse> restore_document(document_id)

Restore Document

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
document_id = 'document_id_example' # String | 

begin
  # Restore Document
  result = api_instance.restore_document(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->restore_document: #{e}"
end
```

#### Using the restore_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> restore_document_with_http_info(document_id)

```ruby
begin
  # Restore Document
  data, status_code, headers = api_instance.restore_document_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->restore_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_document

> <DeliveryResponse> send_document(document_id, delivery_send_request)

Send Document

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
document_id = 'document_id_example' # String | 
delivery_send_request = InvoicePDFs::DeliverySendRequest.new({to: ["client@example.com"]}) # DeliverySendRequest | 

begin
  # Send Document
  result = api_instance.send_document(document_id, delivery_send_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->send_document: #{e}"
end
```

#### Using the send_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryResponse>, Integer, Hash)> send_document_with_http_info(document_id, delivery_send_request)

```ruby
begin
  # Send Document
  data, status_code, headers = api_instance.send_document_with_http_info(document_id, delivery_send_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->send_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **delivery_send_request** | [**DeliverySendRequest**](DeliverySendRequest.md) |  |  |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## update_document

> <DocumentResponse> update_document(document_id, document_patch_request)

Update Document

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
document_id = 'document_id_example' # String | 
document_patch_request = InvoicePDFs::DocumentPatchRequest.new # DocumentPatchRequest | 

begin
  # Update Document
  result = api_instance.update_document(document_id, document_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->update_document: #{e}"
end
```

#### Using the update_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> update_document_with_http_info(document_id, document_patch_request)

```ruby
begin
  # Update Document
  data, status_code, headers = api_instance.update_document_with_http_info(document_id, document_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->update_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **document_patch_request** | [**DocumentPatchRequest**](DocumentPatchRequest.md) |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## validate_document

> <DocumentValidateResponse> validate_document(document_validate_request)

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
  result = api_instance.validate_document(document_validate_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->validate_document: #{e}"
end
```

#### Using the validate_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentValidateResponse>, Integer, Hash)> validate_document_with_http_info(document_validate_request)

```ruby
begin
  # Validate Document
  data, status_code, headers = api_instance.validate_document_with_http_info(document_validate_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentValidateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->validate_document_with_http_info: #{e}"
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


## void_document

> <DocumentResponse> void_document(document_id)

Void Document

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
document_id = 'document_id_example' # String | 

begin
  # Void Document
  result = api_instance.void_document(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->void_document: #{e}"
end
```

#### Using the void_document_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> void_document_with_http_info(document_id)

```ruby
begin
  # Void Document
  data, status_code, headers = api_instance.void_document_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->void_document_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**DocumentResponse**](DocumentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

