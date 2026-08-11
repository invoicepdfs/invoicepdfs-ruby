# InvoicePDFs::RecurringInvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_recurring_invoice**](RecurringInvoicesApi.md#cancel_recurring_invoice) | **DELETE** /api/v1/recurring-invoices/{recurring_id} | Cancel Recurring Invoice |
| [**create_recurring_invoice**](RecurringInvoicesApi.md#create_recurring_invoice) | **POST** /api/v1/recurring-invoices | Create Recurring Invoice |
| [**get_recurring_invoice**](RecurringInvoicesApi.md#get_recurring_invoice) | **GET** /api/v1/recurring-invoices/{recurring_id} | Get Recurring Invoice |
| [**list_generated_invoices**](RecurringInvoicesApi.md#list_generated_invoices) | **GET** /api/v1/recurring-invoices/{recurring_id}/invoices | List Generated Invoices |
| [**list_recurring_invoices**](RecurringInvoicesApi.md#list_recurring_invoices) | **GET** /api/v1/recurring-invoices | List Recurring Invoices |
| [**pause_recurring_invoice**](RecurringInvoicesApi.md#pause_recurring_invoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/pause | Pause Recurring Invoice |
| [**resume_recurring_invoice**](RecurringInvoicesApi.md#resume_recurring_invoice) | **POST** /api/v1/recurring-invoices/{recurring_id}/resume | Resume Recurring Invoice |
| [**update_recurring_invoice**](RecurringInvoicesApi.md#update_recurring_invoice) | **PATCH** /api/v1/recurring-invoices/{recurring_id} | Update Recurring Invoice |


## cancel_recurring_invoice

> <RecurringInvoiceResponse> cancel_recurring_invoice(recurring_id)

Cancel Recurring Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
recurring_id = 'recurring_id_example' # String | 

begin
  # Cancel Recurring Invoice
  result = api_instance.cancel_recurring_invoice(recurring_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->cancel_recurring_invoice: #{e}"
end
```

#### Using the cancel_recurring_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringInvoiceResponse>, Integer, Hash)> cancel_recurring_invoice_with_http_info(recurring_id)

```ruby
begin
  # Cancel Recurring Invoice
  data, status_code, headers = api_instance.cancel_recurring_invoice_with_http_info(recurring_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringInvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->cancel_recurring_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recurring_id** | **String** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## create_recurring_invoice

> <RecurringInvoiceResponse> create_recurring_invoice(recurring_invoice_create_request)

Create Recurring Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
recurring_invoice_create_request = InvoicePDFs::RecurringInvoiceCreateRequest.new({business_profile_id: 'business_profile_id_example', customer_id: 'customer_id_example', frequency: 'frequency_example', start_date: Date.today, invoice_template: InvoicePDFs::InvoiceDraftRequest.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', business_profile_id: 'bp_01ABC', customer_id: 'cus_01XYZ', line_items: [InvoicePDFs::InvoiceLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]})}) # RecurringInvoiceCreateRequest | 

begin
  # Create Recurring Invoice
  result = api_instance.create_recurring_invoice(recurring_invoice_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->create_recurring_invoice: #{e}"
end
```

#### Using the create_recurring_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringInvoiceResponse>, Integer, Hash)> create_recurring_invoice_with_http_info(recurring_invoice_create_request)

```ruby
begin
  # Create Recurring Invoice
  data, status_code, headers = api_instance.create_recurring_invoice_with_http_info(recurring_invoice_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringInvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->create_recurring_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recurring_invoice_create_request** | [**RecurringInvoiceCreateRequest**](RecurringInvoiceCreateRequest.md) |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## get_recurring_invoice

> <RecurringInvoiceResponse> get_recurring_invoice(recurring_id)

Get Recurring Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
recurring_id = 'recurring_id_example' # String | 

begin
  # Get Recurring Invoice
  result = api_instance.get_recurring_invoice(recurring_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->get_recurring_invoice: #{e}"
end
```

#### Using the get_recurring_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringInvoiceResponse>, Integer, Hash)> get_recurring_invoice_with_http_info(recurring_id)

```ruby
begin
  # Get Recurring Invoice
  data, status_code, headers = api_instance.get_recurring_invoice_with_http_info(recurring_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringInvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->get_recurring_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recurring_id** | **String** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_generated_invoices

> <InvoicesListResponse> list_generated_invoices(recurring_id, opts)

List Generated Invoices

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
recurring_id = 'recurring_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Generated Invoices
  result = api_instance.list_generated_invoices(recurring_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->list_generated_invoices: #{e}"
end
```

#### Using the list_generated_invoices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoicesListResponse>, Integer, Hash)> list_generated_invoices_with_http_info(recurring_id, opts)

```ruby
begin
  # List Generated Invoices
  data, status_code, headers = api_instance.list_generated_invoices_with_http_info(recurring_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoicesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->list_generated_invoices_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recurring_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**InvoicesListResponse**](InvoicesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_recurring_invoices

> <RecurringInvoicesListResponse> list_recurring_invoices(opts)

List Recurring Invoices

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example', # String | 
  status: 'status_example' # String | 
}

begin
  # List Recurring Invoices
  result = api_instance.list_recurring_invoices(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->list_recurring_invoices: #{e}"
end
```

#### Using the list_recurring_invoices_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringInvoicesListResponse>, Integer, Hash)> list_recurring_invoices_with_http_info(opts)

```ruby
begin
  # List Recurring Invoices
  data, status_code, headers = api_instance.list_recurring_invoices_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringInvoicesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->list_recurring_invoices_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |

### Return type

[**RecurringInvoicesListResponse**](RecurringInvoicesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## pause_recurring_invoice

> <RecurringInvoiceResponse> pause_recurring_invoice(recurring_id)

Pause Recurring Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
recurring_id = 'recurring_id_example' # String | 

begin
  # Pause Recurring Invoice
  result = api_instance.pause_recurring_invoice(recurring_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->pause_recurring_invoice: #{e}"
end
```

#### Using the pause_recurring_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringInvoiceResponse>, Integer, Hash)> pause_recurring_invoice_with_http_info(recurring_id)

```ruby
begin
  # Pause Recurring Invoice
  data, status_code, headers = api_instance.pause_recurring_invoice_with_http_info(recurring_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringInvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->pause_recurring_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recurring_id** | **String** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## resume_recurring_invoice

> <RecurringInvoiceResponse> resume_recurring_invoice(recurring_id)

Resume Recurring Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
recurring_id = 'recurring_id_example' # String | 

begin
  # Resume Recurring Invoice
  result = api_instance.resume_recurring_invoice(recurring_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->resume_recurring_invoice: #{e}"
end
```

#### Using the resume_recurring_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringInvoiceResponse>, Integer, Hash)> resume_recurring_invoice_with_http_info(recurring_id)

```ruby
begin
  # Resume Recurring Invoice
  data, status_code, headers = api_instance.resume_recurring_invoice_with_http_info(recurring_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringInvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->resume_recurring_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recurring_id** | **String** |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_recurring_invoice

> <RecurringInvoiceResponse> update_recurring_invoice(recurring_id, recurring_invoice_patch_request)

Update Recurring Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::RecurringInvoicesApi.new
recurring_id = 'recurring_id_example' # String | 
recurring_invoice_patch_request = InvoicePDFs::RecurringInvoicePatchRequest.new # RecurringInvoicePatchRequest | 

begin
  # Update Recurring Invoice
  result = api_instance.update_recurring_invoice(recurring_id, recurring_invoice_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->update_recurring_invoice: #{e}"
end
```

#### Using the update_recurring_invoice_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<RecurringInvoiceResponse>, Integer, Hash)> update_recurring_invoice_with_http_info(recurring_id, recurring_invoice_patch_request)

```ruby
begin
  # Update Recurring Invoice
  data, status_code, headers = api_instance.update_recurring_invoice_with_http_info(recurring_id, recurring_invoice_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <RecurringInvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling RecurringInvoicesApi->update_recurring_invoice_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **recurring_id** | **String** |  |  |
| **recurring_invoice_patch_request** | [**RecurringInvoicePatchRequest**](RecurringInvoicePatchRequest.md) |  |  |

### Return type

[**RecurringInvoiceResponse**](RecurringInvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

