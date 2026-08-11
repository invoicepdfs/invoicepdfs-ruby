# InvoicePDFs::FilesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**delete_file**](FilesApi.md#delete_file) | **DELETE** /api/v1/files/{file_id} | Delete File |
| [**get_file**](FilesApi.md#get_file) | **GET** /api/v1/files/{file_id} | Get File |
| [**upload_file**](FilesApi.md#upload_file) | **POST** /api/v1/files | Upload File |


## delete_file

> <SimpleBoolResponse> delete_file(file_id)

Delete File

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::FilesApi.new
file_id = 'file_id_example' # String | 

begin
  # Delete File
  result = api_instance.delete_file(file_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling FilesApi->delete_file: #{e}"
end
```

#### Using the delete_file_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_file_with_http_info(file_id)

```ruby
begin
  # Delete File
  data, status_code, headers = api_instance.delete_file_with_http_info(file_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling FilesApi->delete_file_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_file

> <FileResponse> get_file(file_id)

Get File

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::FilesApi.new
file_id = 'file_id_example' # String | 

begin
  # Get File
  result = api_instance.get_file(file_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling FilesApi->get_file: #{e}"
end
```

#### Using the get_file_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FileResponse>, Integer, Hash)> get_file_with_http_info(file_id)

```ruby
begin
  # Get File
  data, status_code, headers = api_instance.get_file_with_http_info(file_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling FilesApi->get_file_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file_id** | **String** |  |  |

### Return type

[**FileResponse**](FileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## upload_file

> <FileResponse> upload_file(file, opts)

Upload File

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::FilesApi.new
file = File.new('/path/to/some/file') # File | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Upload File
  result = api_instance.upload_file(file, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling FilesApi->upload_file: #{e}"
end
```

#### Using the upload_file_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<FileResponse>, Integer, Hash)> upload_file_with_http_info(file, opts)

```ruby
begin
  # Upload File
  data, status_code, headers = api_instance.upload_file_with_http_info(file, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <FileResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling FilesApi->upload_file_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file** | **File** |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**FileResponse**](FileResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

