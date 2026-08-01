# InvoicePDFs::PaymentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_payment_api_v1_documents_invoice_id_payments_post**](PaymentsApi.md#create_payment_api_v1_documents_invoice_id_payments_post) | **POST** /api/v1/documents/{invoice_id}/payments | Create Payment |
| [**delete_payment_api_v1_payments_payment_id_delete**](PaymentsApi.md#delete_payment_api_v1_payments_payment_id_delete) | **DELETE** /api/v1/payments/{payment_id} | Delete Payment |
| [**get_payment_api_v1_payments_payment_id_get**](PaymentsApi.md#get_payment_api_v1_payments_payment_id_get) | **GET** /api/v1/payments/{payment_id} | Get Payment |
| [**list_invoice_payments_api_v1_documents_invoice_id_payments_get**](PaymentsApi.md#list_invoice_payments_api_v1_documents_invoice_id_payments_get) | **GET** /api/v1/documents/{invoice_id}/payments | List Invoice Payments |
| [**update_payment_api_v1_payments_payment_id_patch**](PaymentsApi.md#update_payment_api_v1_payments_payment_id_patch) | **PATCH** /api/v1/payments/{payment_id} | Update Payment |


## create_payment_api_v1_documents_invoice_id_payments_post

> <PaymentResponse> create_payment_api_v1_documents_invoice_id_payments_post(invoice_id, payment_create_request)

Create Payment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::PaymentsApi.new
invoice_id = 'invoice_id_example' # String | 
payment_create_request = InvoicePDFs::PaymentCreateRequest.new({amount: '53.10', paid_at: Time.parse('2026-07-17T18:30Z')}) # PaymentCreateRequest | 

begin
  # Create Payment
  result = api_instance.create_payment_api_v1_documents_invoice_id_payments_post(invoice_id, payment_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->create_payment_api_v1_documents_invoice_id_payments_post: #{e}"
end
```

#### Using the create_payment_api_v1_documents_invoice_id_payments_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentResponse>, Integer, Hash)> create_payment_api_v1_documents_invoice_id_payments_post_with_http_info(invoice_id, payment_create_request)

```ruby
begin
  # Create Payment
  data, status_code, headers = api_instance.create_payment_api_v1_documents_invoice_id_payments_post_with_http_info(invoice_id, payment_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->create_payment_api_v1_documents_invoice_id_payments_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **payment_create_request** | [**PaymentCreateRequest**](PaymentCreateRequest.md) |  |  |

### Return type

[**PaymentResponse**](PaymentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_payment_api_v1_payments_payment_id_delete

> <SimpleBoolResponse> delete_payment_api_v1_payments_payment_id_delete(payment_id)

Delete Payment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::PaymentsApi.new
payment_id = 'payment_id_example' # String | 

begin
  # Delete Payment
  result = api_instance.delete_payment_api_v1_payments_payment_id_delete(payment_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->delete_payment_api_v1_payments_payment_id_delete: #{e}"
end
```

#### Using the delete_payment_api_v1_payments_payment_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_payment_api_v1_payments_payment_id_delete_with_http_info(payment_id)

```ruby
begin
  # Delete Payment
  data, status_code, headers = api_instance.delete_payment_api_v1_payments_payment_id_delete_with_http_info(payment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->delete_payment_api_v1_payments_payment_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payment_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_payment_api_v1_payments_payment_id_get

> <PaymentResponse> get_payment_api_v1_payments_payment_id_get(payment_id)

Get Payment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::PaymentsApi.new
payment_id = 'payment_id_example' # String | 

begin
  # Get Payment
  result = api_instance.get_payment_api_v1_payments_payment_id_get(payment_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->get_payment_api_v1_payments_payment_id_get: #{e}"
end
```

#### Using the get_payment_api_v1_payments_payment_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentResponse>, Integer, Hash)> get_payment_api_v1_payments_payment_id_get_with_http_info(payment_id)

```ruby
begin
  # Get Payment
  data, status_code, headers = api_instance.get_payment_api_v1_payments_payment_id_get_with_http_info(payment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->get_payment_api_v1_payments_payment_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payment_id** | **String** |  |  |

### Return type

[**PaymentResponse**](PaymentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_invoice_payments_api_v1_documents_invoice_id_payments_get

> <PaymentsListResponse> list_invoice_payments_api_v1_documents_invoice_id_payments_get(invoice_id, opts)

List Invoice Payments

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::PaymentsApi.new
invoice_id = 'invoice_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Invoice Payments
  result = api_instance.list_invoice_payments_api_v1_documents_invoice_id_payments_get(invoice_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->list_invoice_payments_api_v1_documents_invoice_id_payments_get: #{e}"
end
```

#### Using the list_invoice_payments_api_v1_documents_invoice_id_payments_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentsListResponse>, Integer, Hash)> list_invoice_payments_api_v1_documents_invoice_id_payments_get_with_http_info(invoice_id, opts)

```ruby
begin
  # List Invoice Payments
  data, status_code, headers = api_instance.list_invoice_payments_api_v1_documents_invoice_id_payments_get_with_http_info(invoice_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->list_invoice_payments_api_v1_documents_invoice_id_payments_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**PaymentsListResponse**](PaymentsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_payment_api_v1_payments_payment_id_patch

> <PaymentResponse> update_payment_api_v1_payments_payment_id_patch(payment_id, payment_patch_request)

Update Payment

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::PaymentsApi.new
payment_id = 'payment_id_example' # String | 
payment_patch_request = InvoicePDFs::PaymentPatchRequest.new # PaymentPatchRequest | 

begin
  # Update Payment
  result = api_instance.update_payment_api_v1_payments_payment_id_patch(payment_id, payment_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->update_payment_api_v1_payments_payment_id_patch: #{e}"
end
```

#### Using the update_payment_api_v1_payments_payment_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentResponse>, Integer, Hash)> update_payment_api_v1_payments_payment_id_patch_with_http_info(payment_id, payment_patch_request)

```ruby
begin
  # Update Payment
  data, status_code, headers = api_instance.update_payment_api_v1_payments_payment_id_patch_with_http_info(payment_id, payment_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->update_payment_api_v1_payments_payment_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payment_id** | **String** |  |  |
| **payment_patch_request** | [**PaymentPatchRequest**](PaymentPatchRequest.md) |  |  |

### Return type

[**PaymentResponse**](PaymentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

