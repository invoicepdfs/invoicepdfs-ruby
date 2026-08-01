# InvoicePDFs::CreditNotesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_credit_note_api_v1_credit_notes_post**](CreditNotesApi.md#create_credit_note_api_v1_credit_notes_post) | **POST** /api/v1/credit-notes | Create Credit Note |
| [**finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post**](CreditNotesApi.md#finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post) | **POST** /api/v1/credit-notes/{credit_note_id}/finalize | Finalize Credit Note |
| [**get_credit_note_api_v1_credit_notes_credit_note_id_get**](CreditNotesApi.md#get_credit_note_api_v1_credit_notes_credit_note_id_get) | **GET** /api/v1/credit-notes/{credit_note_id} | Get Credit Note |
| [**list_credit_notes_api_v1_credit_notes_get**](CreditNotesApi.md#list_credit_notes_api_v1_credit_notes_get) | **GET** /api/v1/credit-notes | List Credit Notes |
| [**render_credit_note_api_v1_credit_notes_credit_note_id_renders_post**](CreditNotesApi.md#render_credit_note_api_v1_credit_notes_credit_note_id_renders_post) | **POST** /api/v1/credit-notes/{credit_note_id}/renders | Render Credit Note |


## create_credit_note_api_v1_credit_notes_post

> <CreditNoteResponse> create_credit_note_api_v1_credit_notes_post(credit_note_create_request)

Create Credit Note

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CreditNotesApi.new
credit_note_create_request = InvoicePDFs::CreditNoteCreateRequest.new({invoice_id: 'inv_01ABC', credit_note_number: 'CN-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), line_items: [InvoicePDFs::CreditNoteLineItemInput.new({name: 'Web Development', quantity: '1', unit_price: '150.00'})]}) # CreditNoteCreateRequest | 

begin
  # Create Credit Note
  result = api_instance.create_credit_note_api_v1_credit_notes_post(credit_note_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->create_credit_note_api_v1_credit_notes_post: #{e}"
end
```

#### Using the create_credit_note_api_v1_credit_notes_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreditNoteResponse>, Integer, Hash)> create_credit_note_api_v1_credit_notes_post_with_http_info(credit_note_create_request)

```ruby
begin
  # Create Credit Note
  data, status_code, headers = api_instance.create_credit_note_api_v1_credit_notes_post_with_http_info(credit_note_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreditNoteResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->create_credit_note_api_v1_credit_notes_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credit_note_create_request** | [**CreditNoteCreateRequest**](CreditNoteCreateRequest.md) |  |  |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post

> <CreditNoteResponse> finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post(credit_note_id)

Finalize Credit Note

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CreditNotesApi.new
credit_note_id = 'credit_note_id_example' # String | 

begin
  # Finalize Credit Note
  result = api_instance.finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post(credit_note_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post: #{e}"
end
```

#### Using the finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreditNoteResponse>, Integer, Hash)> finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post_with_http_info(credit_note_id)

```ruby
begin
  # Finalize Credit Note
  data, status_code, headers = api_instance.finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post_with_http_info(credit_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreditNoteResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->finalize_credit_note_api_v1_credit_notes_credit_note_id_finalize_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credit_note_id** | **String** |  |  |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_credit_note_api_v1_credit_notes_credit_note_id_get

> <CreditNoteResponse> get_credit_note_api_v1_credit_notes_credit_note_id_get(credit_note_id)

Get Credit Note

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CreditNotesApi.new
credit_note_id = 'credit_note_id_example' # String | 

begin
  # Get Credit Note
  result = api_instance.get_credit_note_api_v1_credit_notes_credit_note_id_get(credit_note_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->get_credit_note_api_v1_credit_notes_credit_note_id_get: #{e}"
end
```

#### Using the get_credit_note_api_v1_credit_notes_credit_note_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreditNoteResponse>, Integer, Hash)> get_credit_note_api_v1_credit_notes_credit_note_id_get_with_http_info(credit_note_id)

```ruby
begin
  # Get Credit Note
  data, status_code, headers = api_instance.get_credit_note_api_v1_credit_notes_credit_note_id_get_with_http_info(credit_note_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreditNoteResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->get_credit_note_api_v1_credit_notes_credit_note_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credit_note_id** | **String** |  |  |

### Return type

[**CreditNoteResponse**](CreditNoteResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_credit_notes_api_v1_credit_notes_get

> <CreditNotesListResponse> list_credit_notes_api_v1_credit_notes_get(opts)

List Credit Notes

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CreditNotesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Credit Notes
  result = api_instance.list_credit_notes_api_v1_credit_notes_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->list_credit_notes_api_v1_credit_notes_get: #{e}"
end
```

#### Using the list_credit_notes_api_v1_credit_notes_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CreditNotesListResponse>, Integer, Hash)> list_credit_notes_api_v1_credit_notes_get_with_http_info(opts)

```ruby
begin
  # List Credit Notes
  data, status_code, headers = api_instance.list_credit_notes_api_v1_credit_notes_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CreditNotesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->list_credit_notes_api_v1_credit_notes_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**CreditNotesListResponse**](CreditNotesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## render_credit_note_api_v1_credit_notes_credit_note_id_renders_post

> Object render_credit_note_api_v1_credit_notes_credit_note_id_renders_post(credit_note_id, opts)

Render Credit Note

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CreditNotesApi.new
credit_note_id = 'credit_note_id_example' # String | 
opts = {
  credit_note_render_request: InvoicePDFs::CreditNoteRenderRequest.new # CreditNoteRenderRequest | 
}

begin
  # Render Credit Note
  result = api_instance.render_credit_note_api_v1_credit_notes_credit_note_id_renders_post(credit_note_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->render_credit_note_api_v1_credit_notes_credit_note_id_renders_post: #{e}"
end
```

#### Using the render_credit_note_api_v1_credit_notes_credit_note_id_renders_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> render_credit_note_api_v1_credit_notes_credit_note_id_renders_post_with_http_info(credit_note_id, opts)

```ruby
begin
  # Render Credit Note
  data, status_code, headers = api_instance.render_credit_note_api_v1_credit_notes_credit_note_id_renders_post_with_http_info(credit_note_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CreditNotesApi->render_credit_note_api_v1_credit_notes_credit_note_id_renders_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **credit_note_id** | **String** |  |  |
| **credit_note_render_request** | [**CreditNoteRenderRequest**](CreditNoteRenderRequest.md) |  | [optional] |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

