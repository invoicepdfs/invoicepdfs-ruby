# InvoicePDFs::RendersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**download_render**](RendersApi.md#download_render) | **GET** /api/v1/renders/{render_id}/download | Download Render |
| [**get_render**](RendersApi.md#get_render) | **GET** /api/v1/renders/{render_id} | Get Render |


## download_render

> File download_render(render_id, opts)

Download Render

Fetch the PDF, by signature or by API key.  Two ways in, and the signature is checked *first* — before the row is looked up — so a forged token cannot be used to tell a real render id from an invented one. It also means the token path costs no auth work at all, which matters because this is the one endpoint a browser hits directly.

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
opts = {
  token: 'token_example' # String | The signature from this render's `download_url`. Present it and no API key is needed — that is what makes the URL a link. Omit it and the request authenticates normally.
}

begin
  # Download Render
  result = api_instance.download_render(render_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->download_render: #{e}"
end
```

#### Using the download_render_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(File, Integer, Hash)> download_render_with_http_info(render_id, opts)

```ruby
begin
  # Download Render
  data, status_code, headers = api_instance.download_render_with_http_info(render_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => File
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->download_render_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **render_id** | **String** |  |  |
| **token** | **String** | The signature from this render&#39;s &#x60;download_url&#x60;. Present it and no API key is needed — that is what makes the URL a link. Omit it and the request authenticates normally. | [optional] |

### Return type

**File**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json


## get_render

> <RenderResponse> get_render(render_id)

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
  result = api_instance.get_render(render_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->get_render: #{e}"
end
```

#### Using the get_render_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RenderResponse>, Integer, Hash)> get_render_with_http_info(render_id)

```ruby
begin
  # Get Render
  data, status_code, headers = api_instance.get_render_with_http_info(render_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RenderResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RendersApi->get_render_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **render_id** | **String** |  |  |

### Return type

[**RenderResponse**](RenderResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

