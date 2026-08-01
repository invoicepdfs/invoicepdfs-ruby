# InvoicePDFs::CustomersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_customer_api_v1_customers_post**](CustomersApi.md#create_customer_api_v1_customers_post) | **POST** /api/v1/customers | Create Customer |
| [**delete_customer_api_v1_customers_customer_id_delete**](CustomersApi.md#delete_customer_api_v1_customers_customer_id_delete) | **DELETE** /api/v1/customers/{customer_id} | Delete Customer |
| [**get_customer_api_v1_customers_customer_id_get**](CustomersApi.md#get_customer_api_v1_customers_customer_id_get) | **GET** /api/v1/customers/{customer_id} | Get Customer |
| [**list_customers_api_v1_customers_get**](CustomersApi.md#list_customers_api_v1_customers_get) | **GET** /api/v1/customers | List Customers |
| [**patch_customer_api_v1_customers_customer_id_patch**](CustomersApi.md#patch_customer_api_v1_customers_customer_id_patch) | **PATCH** /api/v1/customers/{customer_id} | Patch Customer |


## create_customer_api_v1_customers_post

> <CustomerResponse> create_customer_api_v1_customers_post(customer_create, opts)

Create Customer

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CustomersApi.new
customer_create = InvoicePDFs::CustomerCreate.new({name: 'Jane Smith'}) # CustomerCreate | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Create Customer
  result = api_instance.create_customer_api_v1_customers_post(customer_create, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->create_customer_api_v1_customers_post: #{e}"
end
```

#### Using the create_customer_api_v1_customers_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponse>, Integer, Hash)> create_customer_api_v1_customers_post_with_http_info(customer_create, opts)

```ruby
begin
  # Create Customer
  data, status_code, headers = api_instance.create_customer_api_v1_customers_post_with_http_info(customer_create, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->create_customer_api_v1_customers_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_create** | [**CustomerCreate**](CustomerCreate.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**CustomerResponse**](CustomerResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_customer_api_v1_customers_customer_id_delete

> <SimpleBoolResponse> delete_customer_api_v1_customers_customer_id_delete(customer_id)

Delete Customer

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CustomersApi.new
customer_id = 'customer_id_example' # String | 

begin
  # Delete Customer
  result = api_instance.delete_customer_api_v1_customers_customer_id_delete(customer_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->delete_customer_api_v1_customers_customer_id_delete: #{e}"
end
```

#### Using the delete_customer_api_v1_customers_customer_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_customer_api_v1_customers_customer_id_delete_with_http_info(customer_id)

```ruby
begin
  # Delete Customer
  data, status_code, headers = api_instance.delete_customer_api_v1_customers_customer_id_delete_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->delete_customer_api_v1_customers_customer_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_customer_api_v1_customers_customer_id_get

> <CustomerResponse> get_customer_api_v1_customers_customer_id_get(customer_id)

Get Customer

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CustomersApi.new
customer_id = 'customer_id_example' # String | 

begin
  # Get Customer
  result = api_instance.get_customer_api_v1_customers_customer_id_get(customer_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->get_customer_api_v1_customers_customer_id_get: #{e}"
end
```

#### Using the get_customer_api_v1_customers_customer_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponse>, Integer, Hash)> get_customer_api_v1_customers_customer_id_get_with_http_info(customer_id)

```ruby
begin
  # Get Customer
  data, status_code, headers = api_instance.get_customer_api_v1_customers_customer_id_get_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->get_customer_api_v1_customers_customer_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |

### Return type

[**CustomerResponse**](CustomerResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_customers_api_v1_customers_get

> <CustomersListResponse> list_customers_api_v1_customers_get(opts)

List Customers

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CustomersApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Customers
  result = api_instance.list_customers_api_v1_customers_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->list_customers_api_v1_customers_get: #{e}"
end
```

#### Using the list_customers_api_v1_customers_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomersListResponse>, Integer, Hash)> list_customers_api_v1_customers_get_with_http_info(opts)

```ruby
begin
  # List Customers
  data, status_code, headers = api_instance.list_customers_api_v1_customers_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomersListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->list_customers_api_v1_customers_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**CustomersListResponse**](CustomersListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_customer_api_v1_customers_customer_id_patch

> <CustomerResponse> patch_customer_api_v1_customers_customer_id_patch(customer_id, customer_patch, opts)

Patch Customer

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::CustomersApi.new
customer_id = 'customer_id_example' # String | 
customer_patch = InvoicePDFs::CustomerPatch.new # CustomerPatch | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Patch Customer
  result = api_instance.patch_customer_api_v1_customers_customer_id_patch(customer_id, customer_patch, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->patch_customer_api_v1_customers_customer_id_patch: #{e}"
end
```

#### Using the patch_customer_api_v1_customers_customer_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponse>, Integer, Hash)> patch_customer_api_v1_customers_customer_id_patch_with_http_info(customer_id, customer_patch, opts)

```ruby
begin
  # Patch Customer
  data, status_code, headers = api_instance.patch_customer_api_v1_customers_customer_id_patch_with_http_info(customer_id, customer_patch, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->patch_customer_api_v1_customers_customer_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_id** | **String** |  |  |
| **customer_patch** | [**CustomerPatch**](CustomerPatch.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**CustomerResponse**](CustomerResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

