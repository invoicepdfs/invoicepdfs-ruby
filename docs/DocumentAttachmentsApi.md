# InvoicePDFs::DocumentAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_document_attachment**](DocumentAttachmentsApi.md#create_document_attachment) | **POST** /api/v1/documents/{document_id}/attachments | Create Document Attachment |
| [**delete_document_attachment**](DocumentAttachmentsApi.md#delete_document_attachment) | **DELETE** /api/v1/documents/{document_id}/attachments/{attachment_id} | Delete Document Attachment |
| [**list_document_attachments**](DocumentAttachmentsApi.md#list_document_attachments) | **GET** /api/v1/documents/{document_id}/attachments | List Document Attachments |


## create_document_attachment

> <InvoiceAttachmentResponse> create_document_attachment(document_id, invoice_attachment_create_request)

Create Document Attachment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DocumentAttachmentsApi.new
document_id = 'document_id_example' # String | 
invoice_attachment_create_request = InvoicePDFs::InvoiceAttachmentCreateRequest.new({file_id: 'fil_01ABC'}) # InvoiceAttachmentCreateRequest | 

begin
  # Create Document Attachment
  result = api_instance.create_document_attachment(document_id, invoice_attachment_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentAttachmentsApi->create_document_attachment: #{e}"
end
```

#### Using the create_document_attachment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceAttachmentResponse>, Integer, Hash)> create_document_attachment_with_http_info(document_id, invoice_attachment_create_request)

```ruby
begin
  # Create Document Attachment
  data, status_code, headers = api_instance.create_document_attachment_with_http_info(document_id, invoice_attachment_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceAttachmentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentAttachmentsApi->create_document_attachment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **invoice_attachment_create_request** | [**InvoiceAttachmentCreateRequest**](InvoiceAttachmentCreateRequest.md) |  |  |

### Return type

[**InvoiceAttachmentResponse**](InvoiceAttachmentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_document_attachment

> <SimpleBoolResponse> delete_document_attachment(document_id, attachment_id)

Delete Document Attachment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DocumentAttachmentsApi.new
document_id = 'document_id_example' # String | 
attachment_id = 'attachment_id_example' # String | 

begin
  # Delete Document Attachment
  result = api_instance.delete_document_attachment(document_id, attachment_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentAttachmentsApi->delete_document_attachment: #{e}"
end
```

#### Using the delete_document_attachment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_document_attachment_with_http_info(document_id, attachment_id)

```ruby
begin
  # Delete Document Attachment
  data, status_code, headers = api_instance.delete_document_attachment_with_http_info(document_id, attachment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentAttachmentsApi->delete_document_attachment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **attachment_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_document_attachments

> <InvoiceAttachmentsListResponse> list_document_attachments(document_id)

List Document Attachments

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DocumentAttachmentsApi.new
document_id = 'document_id_example' # String | 

begin
  # List Document Attachments
  result = api_instance.list_document_attachments(document_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentAttachmentsApi->list_document_attachments: #{e}"
end
```

#### Using the list_document_attachments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceAttachmentsListResponse>, Integer, Hash)> list_document_attachments_with_http_info(document_id)

```ruby
begin
  # List Document Attachments
  data, status_code, headers = api_instance.list_document_attachments_with_http_info(document_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceAttachmentsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DocumentAttachmentsApi->list_document_attachments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |

### Return type

[**InvoiceAttachmentsListResponse**](InvoiceAttachmentsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

