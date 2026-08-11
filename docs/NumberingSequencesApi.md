# InvoicePDFs::NumberingSequencesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**consume_sequence_number**](NumberingSequencesApi.md#consume_sequence_number) | **POST** /api/v1/numbering-sequences/{sequence_id}/next | Consume Sequence Number |
| [**create_sequence**](NumberingSequencesApi.md#create_sequence) | **POST** /api/v1/numbering-sequences | Create Sequence |
| [**delete_sequence**](NumberingSequencesApi.md#delete_sequence) | **DELETE** /api/v1/numbering-sequences/{sequence_id} | Delete Sequence |
| [**get_sequence**](NumberingSequencesApi.md#get_sequence) | **GET** /api/v1/numbering-sequences/{sequence_id} | Get Sequence |
| [**list_sequences**](NumberingSequencesApi.md#list_sequences) | **GET** /api/v1/numbering-sequences | List Sequences |
| [**preview_sequence**](NumberingSequencesApi.md#preview_sequence) | **POST** /api/v1/numbering-sequences/{sequence_id}/preview | Preview Sequence |
| [**update_sequence**](NumberingSequencesApi.md#update_sequence) | **PATCH** /api/v1/numbering-sequences/{sequence_id} | Update Sequence |


## consume_sequence_number

> <NumberingSequenceResponse> consume_sequence_number(sequence_id)

Consume Sequence Number

Consume and return the next number, incrementing the counter.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::NumberingSequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Consume Sequence Number
  result = api_instance.consume_sequence_number(sequence_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->consume_sequence_number: #{e}"
end
```

#### Using the consume_sequence_number_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<NumberingSequenceResponse>, Integer, Hash)> consume_sequence_number_with_http_info(sequence_id)

```ruby
begin
  # Consume Sequence Number
  data, status_code, headers = api_instance.consume_sequence_number_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <NumberingSequenceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->consume_sequence_number_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_sequence

> <NumberingSequenceResponse> create_sequence(numbering_sequence_create_request)

Create Sequence

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::NumberingSequencesApi.new
numbering_sequence_create_request = InvoicePDFs::NumberingSequenceCreateRequest.new({name: 'Default invoice sequence'}) # NumberingSequenceCreateRequest | 

begin
  # Create Sequence
  result = api_instance.create_sequence(numbering_sequence_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->create_sequence: #{e}"
end
```

#### Using the create_sequence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<NumberingSequenceResponse>, Integer, Hash)> create_sequence_with_http_info(numbering_sequence_create_request)

```ruby
begin
  # Create Sequence
  data, status_code, headers = api_instance.create_sequence_with_http_info(numbering_sequence_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <NumberingSequenceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->create_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **numbering_sequence_create_request** | [**NumberingSequenceCreateRequest**](NumberingSequenceCreateRequest.md) |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_sequence

> <SimpleBoolResponse> delete_sequence(sequence_id)

Delete Sequence

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::NumberingSequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Delete Sequence
  result = api_instance.delete_sequence(sequence_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->delete_sequence: #{e}"
end
```

#### Using the delete_sequence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_sequence_with_http_info(sequence_id)

```ruby
begin
  # Delete Sequence
  data, status_code, headers = api_instance.delete_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->delete_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_sequence

> <NumberingSequenceResponse> get_sequence(sequence_id)

Get Sequence

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::NumberingSequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Get Sequence
  result = api_instance.get_sequence(sequence_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->get_sequence: #{e}"
end
```

#### Using the get_sequence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<NumberingSequenceResponse>, Integer, Hash)> get_sequence_with_http_info(sequence_id)

```ruby
begin
  # Get Sequence
  data, status_code, headers = api_instance.get_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <NumberingSequenceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->get_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_sequences

> <NumberingSequencesListResponse> list_sequences(opts)

List Sequences

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::NumberingSequencesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Sequences
  result = api_instance.list_sequences(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->list_sequences: #{e}"
end
```

#### Using the list_sequences_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<NumberingSequencesListResponse>, Integer, Hash)> list_sequences_with_http_info(opts)

```ruby
begin
  # List Sequences
  data, status_code, headers = api_instance.list_sequences_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <NumberingSequencesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->list_sequences_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**NumberingSequencesListResponse**](NumberingSequencesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## preview_sequence

> <NumberingSequencePreviewResponse> preview_sequence(sequence_id)

Preview Sequence

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::NumberingSequencesApi.new
sequence_id = 'sequence_id_example' # String | 

begin
  # Preview Sequence
  result = api_instance.preview_sequence(sequence_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->preview_sequence: #{e}"
end
```

#### Using the preview_sequence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<NumberingSequencePreviewResponse>, Integer, Hash)> preview_sequence_with_http_info(sequence_id)

```ruby
begin
  # Preview Sequence
  data, status_code, headers = api_instance.preview_sequence_with_http_info(sequence_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <NumberingSequencePreviewResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->preview_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |

### Return type

[**NumberingSequencePreviewResponse**](NumberingSequencePreviewResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_sequence

> <NumberingSequenceResponse> update_sequence(sequence_id, numbering_sequence_patch_request)

Update Sequence

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::NumberingSequencesApi.new
sequence_id = 'sequence_id_example' # String | 
numbering_sequence_patch_request = InvoicePDFs::NumberingSequencePatchRequest.new # NumberingSequencePatchRequest | 

begin
  # Update Sequence
  result = api_instance.update_sequence(sequence_id, numbering_sequence_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->update_sequence: #{e}"
end
```

#### Using the update_sequence_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<NumberingSequenceResponse>, Integer, Hash)> update_sequence_with_http_info(sequence_id, numbering_sequence_patch_request)

```ruby
begin
  # Update Sequence
  data, status_code, headers = api_instance.update_sequence_with_http_info(sequence_id, numbering_sequence_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <NumberingSequenceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling NumberingSequencesApi->update_sequence_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **sequence_id** | **String** |  |  |
| **numbering_sequence_patch_request** | [**NumberingSequencePatchRequest**](NumberingSequencePatchRequest.md) |  |  |

### Return type

[**NumberingSequenceResponse**](NumberingSequenceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

