# InvoicePDFs::DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**archive_document_api_v1_documents_document_id_archive_post**](DocumentsApi.md#archive_document_api_v1_documents_document_id_archive_post) | **POST** /api/v1/documents/{document_id}/archive | Archive Document |
| [**calculate_document_api_v1_documents_calculate_post**](DocumentsApi.md#calculate_document_api_v1_documents_calculate_post) | **POST** /api/v1/documents/calculate | Calculate Document |
| [**create_document_api_v1_documents_post**](DocumentsApi.md#create_document_api_v1_documents_post) | **POST** /api/v1/documents | Create Document |
| [**delete_document_api_v1_documents_document_id_delete**](DocumentsApi.md#delete_document_api_v1_documents_document_id_delete) | **DELETE** /api/v1/documents/{document_id} | Delete Document |
| [**finalize_document_api_v1_documents_document_id_finalize_post**](DocumentsApi.md#finalize_document_api_v1_documents_document_id_finalize_post) | **POST** /api/v1/documents/{document_id}/finalize | Finalize Document |
| [**get_document_api_v1_documents_document_id_get**](DocumentsApi.md#get_document_api_v1_documents_document_id_get) | **GET** /api/v1/documents/{document_id} | Get Document |
| [**list_document_deliveries_api_v1_documents_document_id_deliveries_get**](DocumentsApi.md#list_document_deliveries_api_v1_documents_document_id_deliveries_get) | **GET** /api/v1/documents/{document_id}/deliveries | List Document Deliveries |
| [**list_documents_api_v1_documents_get**](DocumentsApi.md#list_documents_api_v1_documents_get) | **GET** /api/v1/documents | List Documents |
| [**mark_paid_api_v1_documents_document_id_mark_paid_post**](DocumentsApi.md#mark_paid_api_v1_documents_document_id_mark_paid_post) | **POST** /api/v1/documents/{document_id}/mark-paid | Mark Paid |
| [**mark_sent_api_v1_documents_document_id_mark_sent_post**](DocumentsApi.md#mark_sent_api_v1_documents_document_id_mark_sent_post) | **POST** /api/v1/documents/{document_id}/mark-sent | Mark Sent |
| [**mark_unpaid_api_v1_documents_document_id_mark_unpaid_post**](DocumentsApi.md#mark_unpaid_api_v1_documents_document_id_mark_unpaid_post) | **POST** /api/v1/documents/{document_id}/mark-unpaid | Mark Unpaid |
| [**patch_document_api_v1_documents_document_id_patch**](DocumentsApi.md#patch_document_api_v1_documents_document_id_patch) | **PATCH** /api/v1/documents/{document_id} | Patch Document |
| [**render_document_api_v1_documents_document_id_renders_post**](DocumentsApi.md#render_document_api_v1_documents_document_id_renders_post) | **POST** /api/v1/documents/{document_id}/renders | Render Document |
| [**render_document_api_v1_documents_render_post**](DocumentsApi.md#render_document_api_v1_documents_render_post) | **POST** /api/v1/documents/render | Render Document |
| [**restore_document_api_v1_documents_document_id_restore_post**](DocumentsApi.md#restore_document_api_v1_documents_document_id_restore_post) | **POST** /api/v1/documents/{document_id}/restore | Restore Document |
| [**send_document_api_v1_documents_document_id_send_post**](DocumentsApi.md#send_document_api_v1_documents_document_id_send_post) | **POST** /api/v1/documents/{document_id}/send | Send Document |
| [**validate_document_api_v1_documents_validate_post**](DocumentsApi.md#validate_document_api_v1_documents_validate_post) | **POST** /api/v1/documents/validate | Validate Document |
| [**void_document_api_v1_documents_document_id_void_post**](DocumentsApi.md#void_document_api_v1_documents_document_id_void_post) | **POST** /api/v1/documents/{document_id}/void | Void Document |


## archive_document_api_v1_documents_document_id_archive_post

> <DocumentResponse> archive_document_api_v1_documents_document_id_archive_post(document_id)

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
  result = api_instance.archive_document_api_v1_documents_document_id_archive_post(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->archive_document_api_v1_documents_document_id_archive_post: #{e}"
end
```

#### Using the archive_document_api_v1_documents_document_id_archive_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> archive_document_api_v1_documents_document_id_archive_post_with_http_info(document_id)

```ruby
begin
  # Archive Document
  data, status_code, headers = api_instance.archive_document_api_v1_documents_document_id_archive_post_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->archive_document_api_v1_documents_document_id_archive_post_with_http_info: #{e}"
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


## create_document_api_v1_documents_post

> <DocumentResponse> create_document_api_v1_documents_post(document_create_request, opts)

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
  result = api_instance.create_document_api_v1_documents_post(document_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->create_document_api_v1_documents_post: #{e}"
end
```

#### Using the create_document_api_v1_documents_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> create_document_api_v1_documents_post_with_http_info(document_create_request, opts)

```ruby
begin
  # Create Document
  data, status_code, headers = api_instance.create_document_api_v1_documents_post_with_http_info(document_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->create_document_api_v1_documents_post_with_http_info: #{e}"
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


## delete_document_api_v1_documents_document_id_delete

> <SimpleBoolResponse> delete_document_api_v1_documents_document_id_delete(document_id)

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
  result = api_instance.delete_document_api_v1_documents_document_id_delete(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->delete_document_api_v1_documents_document_id_delete: #{e}"
end
```

#### Using the delete_document_api_v1_documents_document_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_document_api_v1_documents_document_id_delete_with_http_info(document_id)

```ruby
begin
  # Delete Document
  data, status_code, headers = api_instance.delete_document_api_v1_documents_document_id_delete_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->delete_document_api_v1_documents_document_id_delete_with_http_info: #{e}"
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


## finalize_document_api_v1_documents_document_id_finalize_post

> <DocumentResponse> finalize_document_api_v1_documents_document_id_finalize_post(document_id)

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
  result = api_instance.finalize_document_api_v1_documents_document_id_finalize_post(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->finalize_document_api_v1_documents_document_id_finalize_post: #{e}"
end
```

#### Using the finalize_document_api_v1_documents_document_id_finalize_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> finalize_document_api_v1_documents_document_id_finalize_post_with_http_info(document_id)

```ruby
begin
  # Finalize Document
  data, status_code, headers = api_instance.finalize_document_api_v1_documents_document_id_finalize_post_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->finalize_document_api_v1_documents_document_id_finalize_post_with_http_info: #{e}"
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


## get_document_api_v1_documents_document_id_get

> <DocumentResponse> get_document_api_v1_documents_document_id_get(document_id)

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
  result = api_instance.get_document_api_v1_documents_document_id_get(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->get_document_api_v1_documents_document_id_get: #{e}"
end
```

#### Using the get_document_api_v1_documents_document_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> get_document_api_v1_documents_document_id_get_with_http_info(document_id)

```ruby
begin
  # Get Document
  data, status_code, headers = api_instance.get_document_api_v1_documents_document_id_get_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->get_document_api_v1_documents_document_id_get_with_http_info: #{e}"
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


## list_document_deliveries_api_v1_documents_document_id_deliveries_get

> <DeliveriesListResponse> list_document_deliveries_api_v1_documents_document_id_deliveries_get(document_id, opts)

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
  result = api_instance.list_document_deliveries_api_v1_documents_document_id_deliveries_get(document_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_document_deliveries_api_v1_documents_document_id_deliveries_get: #{e}"
end
```

#### Using the list_document_deliveries_api_v1_documents_document_id_deliveries_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveriesListResponse>, Integer, Hash)> list_document_deliveries_api_v1_documents_document_id_deliveries_get_with_http_info(document_id, opts)

```ruby
begin
  # List Document Deliveries
  data, status_code, headers = api_instance.list_document_deliveries_api_v1_documents_document_id_deliveries_get_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveriesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_document_deliveries_api_v1_documents_document_id_deliveries_get_with_http_info: #{e}"
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


## list_documents_api_v1_documents_get

> <DocumentsListResponse> list_documents_api_v1_documents_get(opts)

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
  result = api_instance.list_documents_api_v1_documents_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_documents_api_v1_documents_get: #{e}"
end
```

#### Using the list_documents_api_v1_documents_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentsListResponse>, Integer, Hash)> list_documents_api_v1_documents_get_with_http_info(opts)

```ruby
begin
  # List Documents
  data, status_code, headers = api_instance.list_documents_api_v1_documents_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->list_documents_api_v1_documents_get_with_http_info: #{e}"
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


## mark_paid_api_v1_documents_document_id_mark_paid_post

> <DocumentResponse> mark_paid_api_v1_documents_document_id_mark_paid_post(document_id)

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
  result = api_instance.mark_paid_api_v1_documents_document_id_mark_paid_post(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_paid_api_v1_documents_document_id_mark_paid_post: #{e}"
end
```

#### Using the mark_paid_api_v1_documents_document_id_mark_paid_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> mark_paid_api_v1_documents_document_id_mark_paid_post_with_http_info(document_id)

```ruby
begin
  # Mark Paid
  data, status_code, headers = api_instance.mark_paid_api_v1_documents_document_id_mark_paid_post_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_paid_api_v1_documents_document_id_mark_paid_post_with_http_info: #{e}"
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


## mark_sent_api_v1_documents_document_id_mark_sent_post

> <DocumentResponse> mark_sent_api_v1_documents_document_id_mark_sent_post(document_id)

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
  result = api_instance.mark_sent_api_v1_documents_document_id_mark_sent_post(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_sent_api_v1_documents_document_id_mark_sent_post: #{e}"
end
```

#### Using the mark_sent_api_v1_documents_document_id_mark_sent_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> mark_sent_api_v1_documents_document_id_mark_sent_post_with_http_info(document_id)

```ruby
begin
  # Mark Sent
  data, status_code, headers = api_instance.mark_sent_api_v1_documents_document_id_mark_sent_post_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_sent_api_v1_documents_document_id_mark_sent_post_with_http_info: #{e}"
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


## mark_unpaid_api_v1_documents_document_id_mark_unpaid_post

> <DocumentResponse> mark_unpaid_api_v1_documents_document_id_mark_unpaid_post(document_id)

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
  result = api_instance.mark_unpaid_api_v1_documents_document_id_mark_unpaid_post(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_unpaid_api_v1_documents_document_id_mark_unpaid_post: #{e}"
end
```

#### Using the mark_unpaid_api_v1_documents_document_id_mark_unpaid_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> mark_unpaid_api_v1_documents_document_id_mark_unpaid_post_with_http_info(document_id)

```ruby
begin
  # Mark Unpaid
  data, status_code, headers = api_instance.mark_unpaid_api_v1_documents_document_id_mark_unpaid_post_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->mark_unpaid_api_v1_documents_document_id_mark_unpaid_post_with_http_info: #{e}"
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


## patch_document_api_v1_documents_document_id_patch

> <DocumentResponse> patch_document_api_v1_documents_document_id_patch(document_id, document_patch_request)

Patch Document

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
  # Patch Document
  result = api_instance.patch_document_api_v1_documents_document_id_patch(document_id, document_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->patch_document_api_v1_documents_document_id_patch: #{e}"
end
```

#### Using the patch_document_api_v1_documents_document_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> patch_document_api_v1_documents_document_id_patch_with_http_info(document_id, document_patch_request)

```ruby
begin
  # Patch Document
  data, status_code, headers = api_instance.patch_document_api_v1_documents_document_id_patch_with_http_info(document_id, document_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->patch_document_api_v1_documents_document_id_patch_with_http_info: #{e}"
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


## render_document_api_v1_documents_document_id_renders_post

> Object render_document_api_v1_documents_document_id_renders_post(document_id, app_documents_schemas_document_render_request, opts)

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
document_id = 'document_id_example' # String | 
app_documents_schemas_document_render_request = InvoicePDFs::AppDocumentsSchemasDocumentRenderRequest.new # AppDocumentsSchemasDocumentRenderRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Render Document
  result = api_instance.render_document_api_v1_documents_document_id_renders_post(document_id, app_documents_schemas_document_render_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->render_document_api_v1_documents_document_id_renders_post: #{e}"
end
```

#### Using the render_document_api_v1_documents_document_id_renders_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> render_document_api_v1_documents_document_id_renders_post_with_http_info(document_id, app_documents_schemas_document_render_request, opts)

```ruby
begin
  # Render Document
  data, status_code, headers = api_instance.render_document_api_v1_documents_document_id_renders_post_with_http_info(document_id, app_documents_schemas_document_render_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->render_document_api_v1_documents_document_id_renders_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **app_documents_schemas_document_render_request** | [**AppDocumentsSchemasDocumentRenderRequest**](AppDocumentsSchemasDocumentRenderRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## render_document_api_v1_documents_render_post

> Object render_document_api_v1_documents_render_post(app_schemas_v1_document_render_request, opts)

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
app_schemas_v1_document_render_request = InvoicePDFs::AppSchemasV1DocumentRenderRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}), template: InvoicePDFs::DocumentTemplateRef.new({id: 'id_example'})}) # AppSchemasV1DocumentRenderRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Render Document
  result = api_instance.render_document_api_v1_documents_render_post(app_schemas_v1_document_render_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->render_document_api_v1_documents_render_post: #{e}"
end
```

#### Using the render_document_api_v1_documents_render_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> render_document_api_v1_documents_render_post_with_http_info(app_schemas_v1_document_render_request, opts)

```ruby
begin
  # Render Document
  data, status_code, headers = api_instance.render_document_api_v1_documents_render_post_with_http_info(app_schemas_v1_document_render_request, opts)
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
| **app_schemas_v1_document_render_request** | [**AppSchemasV1DocumentRenderRequest**](AppSchemasV1DocumentRenderRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## restore_document_api_v1_documents_document_id_restore_post

> <DocumentResponse> restore_document_api_v1_documents_document_id_restore_post(document_id)

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
  result = api_instance.restore_document_api_v1_documents_document_id_restore_post(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->restore_document_api_v1_documents_document_id_restore_post: #{e}"
end
```

#### Using the restore_document_api_v1_documents_document_id_restore_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> restore_document_api_v1_documents_document_id_restore_post_with_http_info(document_id)

```ruby
begin
  # Restore Document
  data, status_code, headers = api_instance.restore_document_api_v1_documents_document_id_restore_post_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->restore_document_api_v1_documents_document_id_restore_post_with_http_info: #{e}"
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


## send_document_api_v1_documents_document_id_send_post

> <DeliveryResponse> send_document_api_v1_documents_document_id_send_post(document_id, delivery_send_request)

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
  result = api_instance.send_document_api_v1_documents_document_id_send_post(document_id, delivery_send_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->send_document_api_v1_documents_document_id_send_post: #{e}"
end
```

#### Using the send_document_api_v1_documents_document_id_send_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryResponse>, Integer, Hash)> send_document_api_v1_documents_document_id_send_post_with_http_info(document_id, delivery_send_request)

```ruby
begin
  # Send Document
  data, status_code, headers = api_instance.send_document_api_v1_documents_document_id_send_post_with_http_info(document_id, delivery_send_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->send_document_api_v1_documents_document_id_send_post_with_http_info: #{e}"
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


## void_document_api_v1_documents_document_id_void_post

> <DocumentResponse> void_document_api_v1_documents_document_id_void_post(document_id)

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
  result = api_instance.void_document_api_v1_documents_document_id_void_post(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->void_document_api_v1_documents_document_id_void_post: #{e}"
end
```

#### Using the void_document_api_v1_documents_document_id_void_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentResponse>, Integer, Hash)> void_document_api_v1_documents_document_id_void_post_with_http_info(document_id)

```ruby
begin
  # Void Document
  data, status_code, headers = api_instance.void_document_api_v1_documents_document_id_void_post_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentsApi->void_document_api_v1_documents_document_id_void_post_with_http_info: #{e}"
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

