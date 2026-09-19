# InvoicePDFs::BatchesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_batch**](BatchesApi.md#cancel_batch) | **POST** /api/v1/batches/{batch_id}/cancel | Cancel Batch |
| [**create_batch**](BatchesApi.md#create_batch) | **POST** /api/v1/batches | Create Batch |
| [**download_batch**](BatchesApi.md#download_batch) | **GET** /api/v1/batches/{batch_id}/download | Download Batch |
| [**get_batch**](BatchesApi.md#get_batch) | **GET** /api/v1/batches/{batch_id} | Get Batch |
| [**list_batch_items**](BatchesApi.md#list_batch_items) | **GET** /api/v1/batches/{batch_id}/items | List Batch Items |
| [**list_batches**](BatchesApi.md#list_batches) | **GET** /api/v1/batches | List Batches |


## cancel_batch

> <BatchResponse> cancel_batch(batch_id)

Cancel Batch

Stop a batch that has not finished.  Items not yet started are cancelled. An item already rendering completes — the work is done and cancelling it would waste it.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BatchesApi.new
batch_id = 'batch_id_example' # String | 

begin
  # Cancel Batch
  result = api_instance.cancel_batch(batch_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->cancel_batch: #{e}"
end
```

#### Using the cancel_batch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BatchResponse>, Integer, Hash)> cancel_batch_with_http_info(batch_id)

```ruby
begin
  # Cancel Batch
  data, status_code, headers = api_instance.cancel_batch_with_http_info(batch_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BatchResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->cancel_batch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_id** | **String** |  |  |

### Return type

[**BatchResponse**](BatchResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_batch

> <BatchResponse> create_batch(batch_create_request)

Create Batch

Queue many documents to be rendered at once.  Returns `202` — the batch is recorded and a worker renders it; nothing is rendered inside this request. Poll `get_batch` for progress, then `download_batch` for the results.  The whole batch is refused if it would exceed the monthly quota, rather than rendering part of it.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BatchesApi.new
batch_create_request = InvoicePDFs::BatchCreateRequest.new({items: [InvoicePDFs::BatchItemInput.new({data: { key: 3.56}})]}) # BatchCreateRequest | 

begin
  # Create Batch
  result = api_instance.create_batch(batch_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->create_batch: #{e}"
end
```

#### Using the create_batch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BatchResponse>, Integer, Hash)> create_batch_with_http_info(batch_create_request)

```ruby
begin
  # Create Batch
  data, status_code, headers = api_instance.create_batch_with_http_info(batch_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BatchResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->create_batch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_create_request** | [**BatchCreateRequest**](BatchCreateRequest.md) |  |  |

### Return type

[**BatchResponse**](BatchResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## download_batch

> File download_batch(batch_id)

Download Batch

Every completed render in the batch, as a ZIP.  `409` until the batch is `completed`. Items that failed are simply absent, so check `failed_items` rather than counting files.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BatchesApi.new
batch_id = 'batch_id_example' # String | 

begin
  # Download Batch
  result = api_instance.download_batch(batch_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->download_batch: #{e}"
end
```

#### Using the download_batch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> download_batch_with_http_info(batch_id)

```ruby
begin
  # Download Batch
  data, status_code, headers = api_instance.download_batch_with_http_info(batch_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->download_batch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_id** | **String** |  |  |

### Return type

**File**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/zip, application/json


## get_batch

> <BatchResponse> get_batch(batch_id)

Get Batch

A batch's status and its per-item counts.  The poll surface: `total_items`, `completed_items` and `failed_items` say how far it has got without listing every item.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BatchesApi.new
batch_id = 'batch_id_example' # String | 

begin
  # Get Batch
  result = api_instance.get_batch(batch_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->get_batch: #{e}"
end
```

#### Using the get_batch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BatchResponse>, Integer, Hash)> get_batch_with_http_info(batch_id)

```ruby
begin
  # Get Batch
  data, status_code, headers = api_instance.get_batch_with_http_info(batch_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BatchResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->get_batch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_id** | **String** |  |  |

### Return type

[**BatchResponse**](BatchResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_batch_items

> <BatchItemsListResponse> list_batch_items(batch_id, opts)

List Batch Items

Every item in a batch with its own status, newest first.  Where to look when `failed_items` is not zero: each row carries its error and, once rendered, its `render_id`.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BatchesApi.new
batch_id = 'batch_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Batch Items
  result = api_instance.list_batch_items(batch_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->list_batch_items: #{e}"
end
```

#### Using the list_batch_items_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BatchItemsListResponse>, Integer, Hash)> list_batch_items_with_http_info(batch_id, opts)

```ruby
begin
  # List Batch Items
  data, status_code, headers = api_instance.list_batch_items_with_http_info(batch_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BatchItemsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->list_batch_items_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **batch_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**BatchItemsListResponse**](BatchItemsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_batches

> <BatchesListResponse> list_batches(opts)

List Batches

Batch jobs on this account, newest first.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BatchesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Batches
  result = api_instance.list_batches(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->list_batches: #{e}"
end
```

#### Using the list_batches_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BatchesListResponse>, Integer, Hash)> list_batches_with_http_info(opts)

```ruby
begin
  # List Batches
  data, status_code, headers = api_instance.list_batches_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BatchesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BatchesApi->list_batches_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**BatchesListResponse**](BatchesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

