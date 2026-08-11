# InvoicePDFs::PaymentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_document_payment**](PaymentsApi.md#create_document_payment) | **POST** /api/v1/documents/{document_id}/payments | Create Document Payment |
| [**delete_payment**](PaymentsApi.md#delete_payment) | **DELETE** /api/v1/payments/{payment_id} | Delete Payment |
| [**get_payment**](PaymentsApi.md#get_payment) | **GET** /api/v1/payments/{payment_id} | Get Payment |
| [**list_document_payments**](PaymentsApi.md#list_document_payments) | **GET** /api/v1/documents/{document_id}/payments | List Document Payments |
| [**update_payment**](PaymentsApi.md#update_payment) | **PATCH** /api/v1/payments/{payment_id} | Update Payment |


## create_document_payment

> <PaymentResponse> create_document_payment(document_id, payment_create_request)

Create Document Payment

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
document_id = 'document_id_example' # String | 
payment_create_request = InvoicePDFs::PaymentCreateRequest.new({amount: '53.10', paid_at: Time.parse('2026-07-17T18:30Z')}) # PaymentCreateRequest | 

begin
  # Create Document Payment
  result = api_instance.create_document_payment(document_id, payment_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->create_document_payment: #{e}"
end
```

#### Using the create_document_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentResponse>, Integer, Hash)> create_document_payment_with_http_info(document_id, payment_create_request)

```ruby
begin
  # Create Document Payment
  data, status_code, headers = api_instance.create_document_payment_with_http_info(document_id, payment_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->create_document_payment_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **payment_create_request** | [**PaymentCreateRequest**](PaymentCreateRequest.md) |  |  |

### Return type

[**PaymentResponse**](PaymentResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_payment

> <SimpleBoolResponse> delete_payment(payment_id)

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
  result = api_instance.delete_payment(payment_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->delete_payment: #{e}"
end
```

#### Using the delete_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_payment_with_http_info(payment_id)

```ruby
begin
  # Delete Payment
  data, status_code, headers = api_instance.delete_payment_with_http_info(payment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->delete_payment_with_http_info: #{e}"
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


## get_payment

> <PaymentResponse> get_payment(payment_id)

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
  result = api_instance.get_payment(payment_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->get_payment: #{e}"
end
```

#### Using the get_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentResponse>, Integer, Hash)> get_payment_with_http_info(payment_id)

```ruby
begin
  # Get Payment
  data, status_code, headers = api_instance.get_payment_with_http_info(payment_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->get_payment_with_http_info: #{e}"
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


## list_document_payments

> <PaymentsListResponse> list_document_payments(document_id, opts)

List Document Payments

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
document_id = 'document_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Document Payments
  result = api_instance.list_document_payments(document_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->list_document_payments: #{e}"
end
```

#### Using the list_document_payments_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentsListResponse>, Integer, Hash)> list_document_payments_with_http_info(document_id, opts)

```ruby
begin
  # List Document Payments
  data, status_code, headers = api_instance.list_document_payments_with_http_info(document_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->list_document_payments_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**PaymentsListResponse**](PaymentsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_payment

> <PaymentResponse> update_payment(payment_id, payment_patch_request)

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
  result = api_instance.update_payment(payment_id, payment_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->update_payment: #{e}"
end
```

#### Using the update_payment_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<PaymentResponse>, Integer, Hash)> update_payment_with_http_info(payment_id, payment_patch_request)

```ruby
begin
  # Update Payment
  data, status_code, headers = api_instance.update_payment_with_http_info(payment_id, payment_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PaymentResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling PaymentsApi->update_payment_with_http_info: #{e}"
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

