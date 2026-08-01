# InvoicePDFs::RendersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**download_render_api_v1_renders_render_id_download_get**](RendersApi.md#download_render_api_v1_renders_render_id_download_get) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**get_render_api_v1_renders_render_id_get**](RendersApi.md#get_render_api_v1_renders_render_id_get) | **GET** /api/v1/renders/{render_id} | Get Render |


## download_render_api_v1_renders_render_id_download_get

> File download_render_api_v1_renders_render_id_download_get(render_id)

Download Render

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RendersApi.new
render_id = 'render_id_example' # String | 

begin
  # Download Render
  result = api_instance.download_render_api_v1_renders_render_id_download_get(render_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->download_render_api_v1_renders_render_id_download_get: #{e}"
end
```

#### Using the download_render_api_v1_renders_render_id_download_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> download_render_api_v1_renders_render_id_download_get_with_http_info(render_id)

```ruby
begin
  # Download Render
  data, status_code, headers = api_instance.download_render_api_v1_renders_render_id_download_get_with_http_info(render_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->download_render_api_v1_renders_render_id_download_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **render_id** | **String** |  |  |

### Return type

**File**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json


## get_render_api_v1_renders_render_id_get

> Hash&lt;String, Object&gt; get_render_api_v1_renders_render_id_get(render_id)

Get Render

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RendersApi.new
render_id = 'render_id_example' # String | 

begin
  # Get Render
  result = api_instance.get_render_api_v1_renders_render_id_get(render_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->get_render_api_v1_renders_render_id_get: #{e}"
end
```

#### Using the get_render_api_v1_renders_render_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> get_render_api_v1_renders_render_id_get_with_http_info(render_id)

```ruby
begin
  # Get Render
  data, status_code, headers = api_instance.get_render_api_v1_renders_render_id_get_with_http_info(render_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->get_render_api_v1_renders_render_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **render_id** | **String** |  |  |

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

