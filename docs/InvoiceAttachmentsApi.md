# InvoicePDFs::InvoiceAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_attachment_api_v1_invoices_invoice_id_attachments_post**](InvoiceAttachmentsApi.md#create_attachment_api_v1_invoices_invoice_id_attachments_post) | **POST** /api/v1/invoices/{invoice_id}/attachments | Create Attachment |
| [**delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete**](InvoiceAttachmentsApi.md#delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete) | **DELETE** /api/v1/invoices/{invoice_id}/attachments/{attachment_id} | Delete Attachment |
| [**list_attachments_api_v1_invoices_invoice_id_attachments_get**](InvoiceAttachmentsApi.md#list_attachments_api_v1_invoices_invoice_id_attachments_get) | **GET** /api/v1/invoices/{invoice_id}/attachments | List Attachments |


## create_attachment_api_v1_invoices_invoice_id_attachments_post

> <InvoiceAttachmentResponse> create_attachment_api_v1_invoices_invoice_id_attachments_post(invoice_id, invoice_attachment_create_request)

Create Attachment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoiceAttachmentsApi.new
invoice_id = 'invoice_id_example' # String | 
invoice_attachment_create_request = InvoicePDFs::InvoiceAttachmentCreateRequest.new({file_id: 'fil_01ABC'}) # InvoiceAttachmentCreateRequest | 

begin
  # Create Attachment
  result = api_instance.create_attachment_api_v1_invoices_invoice_id_attachments_post(invoice_id, invoice_attachment_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoiceAttachmentsApi->create_attachment_api_v1_invoices_invoice_id_attachments_post: #{e}"
end
```

#### Using the create_attachment_api_v1_invoices_invoice_id_attachments_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceAttachmentResponse>, Integer, Hash)> create_attachment_api_v1_invoices_invoice_id_attachments_post_with_http_info(invoice_id, invoice_attachment_create_request)

```ruby
begin
  # Create Attachment
  data, status_code, headers = api_instance.create_attachment_api_v1_invoices_invoice_id_attachments_post_with_http_info(invoice_id, invoice_attachment_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceAttachmentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoiceAttachmentsApi->create_attachment_api_v1_invoices_invoice_id_attachments_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **invoice_attachment_create_request** | [**InvoiceAttachmentCreateRequest**](InvoiceAttachmentCreateRequest.md) |  |  |

### Return type

[**InvoiceAttachmentResponse**](InvoiceAttachmentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete

> <SimpleBoolResponse> delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete(invoice_id, attachment_id)

Delete Attachment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoiceAttachmentsApi.new
invoice_id = 'invoice_id_example' # String | 
attachment_id = 'attachment_id_example' # String | 

begin
  # Delete Attachment
  result = api_instance.delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete(invoice_id, attachment_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoiceAttachmentsApi->delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete: #{e}"
end
```

#### Using the delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete_with_http_info(invoice_id, attachment_id)

```ruby
begin
  # Delete Attachment
  data, status_code, headers = api_instance.delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete_with_http_info(invoice_id, attachment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoiceAttachmentsApi->delete_attachment_api_v1_invoices_invoice_id_attachments_attachment_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **attachment_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_attachments_api_v1_invoices_invoice_id_attachments_get

> <InvoiceAttachmentsListResponse> list_attachments_api_v1_invoices_invoice_id_attachments_get(invoice_id)

List Attachments

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoiceAttachmentsApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # List Attachments
  result = api_instance.list_attachments_api_v1_invoices_invoice_id_attachments_get(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoiceAttachmentsApi->list_attachments_api_v1_invoices_invoice_id_attachments_get: #{e}"
end
```

#### Using the list_attachments_api_v1_invoices_invoice_id_attachments_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceAttachmentsListResponse>, Integer, Hash)> list_attachments_api_v1_invoices_invoice_id_attachments_get_with_http_info(invoice_id)

```ruby
begin
  # List Attachments
  data, status_code, headers = api_instance.list_attachments_api_v1_invoices_invoice_id_attachments_get_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceAttachmentsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoiceAttachmentsApi->list_attachments_api_v1_invoices_invoice_id_attachments_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceAttachmentsListResponse**](InvoiceAttachmentsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

