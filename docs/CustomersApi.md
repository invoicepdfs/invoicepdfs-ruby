# InvoicePDFs::CustomersApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_customer**](CustomersApi.md#create_customer) | **POST** /api/v1/customers | Create Customer |
| [**delete_customer**](CustomersApi.md#delete_customer) | **DELETE** /api/v1/customers/{customer_id} | Delete Customer |
| [**get_customer**](CustomersApi.md#get_customer) | **GET** /api/v1/customers/{customer_id} | Get Customer |
| [**list_customers**](CustomersApi.md#list_customers) | **GET** /api/v1/customers | List Customers |
| [**update_customer**](CustomersApi.md#update_customer) | **PATCH** /api/v1/customers/{customer_id} | Update Customer |


## create_customer

> <CustomerResponse> create_customer(customer_create, opts)

Create Customer

Store a customer you can bill repeatedly.  `tax_id` and `electronic_address` are what e-invoicing needs: a buyer VAT number and the Peppol identifier a receiver is addressed by. Neither is required for a plain PDF.

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
  result = api_instance.create_customer(customer_create, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->create_customer: #{e}"
end
```

#### Using the create_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponse>, Integer, Hash)> create_customer_with_http_info(customer_create, opts)

```ruby
begin
  # Create Customer
  data, status_code, headers = api_instance.create_customer_with_http_info(customer_create, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->create_customer_with_http_info: #{e}"
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


## delete_customer

> <SimpleBoolResponse> delete_customer(customer_id)

Delete Customer

Remove a customer.  `409` if any document still references them, naming what does. History is kept rather than rewritten.

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
  result = api_instance.delete_customer(customer_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->delete_customer: #{e}"
end
```

#### Using the delete_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_customer_with_http_info(customer_id)

```ruby
begin
  # Delete Customer
  data, status_code, headers = api_instance.delete_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->delete_customer_with_http_info: #{e}"
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


## get_customer

> <CustomerResponse> get_customer(customer_id)

Get Customer

One stored customer.

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
  result = api_instance.get_customer(customer_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->get_customer: #{e}"
end
```

#### Using the get_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponse>, Integer, Hash)> get_customer_with_http_info(customer_id)

```ruby
begin
  # Get Customer
  data, status_code, headers = api_instance.get_customer_with_http_info(customer_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->get_customer_with_http_info: #{e}"
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


## list_customers

> <CustomersListResponse> list_customers(opts)

List Customers

The people and companies you bill, newest first.  Cursor-paginated. A customer is optional — the stateless render endpoints take a buyer inline — but storing one lets a document reference it by id.

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
  result = api_instance.list_customers(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->list_customers: #{e}"
end
```

#### Using the list_customers_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomersListResponse>, Integer, Hash)> list_customers_with_http_info(opts)

```ruby
begin
  # List Customers
  data, status_code, headers = api_instance.list_customers_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomersListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->list_customers_with_http_info: #{e}"
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


## update_customer

> <CustomerResponse> update_customer(customer_id, customer_patch, opts)

Update Customer

Change a stored customer.  Only the fields you send are changed — omit one to leave it alone, send `null` to clear it. Documents already issued keep the details they were issued with; this does not rewrite them.

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
  # Update Customer
  result = api_instance.update_customer(customer_id, customer_patch, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->update_customer: #{e}"
end
```

#### Using the update_customer_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CustomerResponse>, Integer, Hash)> update_customer_with_http_info(customer_id, customer_patch, opts)

```ruby
begin
  # Update Customer
  data, status_code, headers = api_instance.update_customer_with_http_info(customer_id, customer_patch, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CustomerResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling CustomersApi->update_customer_with_http_info: #{e}"
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

