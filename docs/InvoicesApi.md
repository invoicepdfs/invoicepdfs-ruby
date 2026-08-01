# InvoicePDFs::InvoicesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**archive_invoice_api_v1_invoices_invoice_id_archive_post**](InvoicesApi.md#archive_invoice_api_v1_invoices_invoice_id_archive_post) | **POST** /api/v1/invoices/{invoice_id}/archive | Archive Invoice |
| [**calculate_invoice_api_v1_invoices_calculate_post**](InvoicesApi.md#calculate_invoice_api_v1_invoices_calculate_post) | **POST** /api/v1/invoices/calculate | Calculate Invoice |
| [**create_invoice_api_v1_invoices_post**](InvoicesApi.md#create_invoice_api_v1_invoices_post) | **POST** /api/v1/invoices | Create Invoice |
| [**delete_invoice_api_v1_invoices_invoice_id_delete**](InvoicesApi.md#delete_invoice_api_v1_invoices_invoice_id_delete) | **DELETE** /api/v1/invoices/{invoice_id} | Delete Invoice |
| [**duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post**](InvoicesApi.md#duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post) | **POST** /api/v1/invoices/{invoice_id}/duplicate | Duplicate Invoice |
| [**finalize_invoice_api_v1_invoices_invoice_id_finalize_post**](InvoicesApi.md#finalize_invoice_api_v1_invoices_invoice_id_finalize_post) | **POST** /api/v1/invoices/{invoice_id}/finalize | Finalize Invoice |
| [**get_invoice_api_v1_invoices_invoice_id_get**](InvoicesApi.md#get_invoice_api_v1_invoices_invoice_id_get) | **GET** /api/v1/invoices/{invoice_id} | Get Invoice |
| [**list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get**](InvoicesApi.md#list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get) | **GET** /api/v1/invoices/{invoice_id}/deliveries | List Invoice Deliveries |
| [**list_invoices_api_v1_invoices_get**](InvoicesApi.md#list_invoices_api_v1_invoices_get) | **GET** /api/v1/invoices | List Invoices |
| [**mark_paid_api_v1_invoices_invoice_id_mark_paid_post**](InvoicesApi.md#mark_paid_api_v1_invoices_invoice_id_mark_paid_post) | **POST** /api/v1/invoices/{invoice_id}/mark-paid | Mark Paid |
| [**mark_sent_api_v1_invoices_invoice_id_mark_sent_post**](InvoicesApi.md#mark_sent_api_v1_invoices_invoice_id_mark_sent_post) | **POST** /api/v1/invoices/{invoice_id}/mark-sent | Mark Sent |
| [**mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post**](InvoicesApi.md#mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post) | **POST** /api/v1/invoices/{invoice_id}/mark-unpaid | Mark Unpaid |
| [**patch_invoice_api_v1_invoices_invoice_id_patch**](InvoicesApi.md#patch_invoice_api_v1_invoices_invoice_id_patch) | **PATCH** /api/v1/invoices/{invoice_id} | Patch Invoice |
| [**preview_invoice_api_v1_invoices_preview_post**](InvoicesApi.md#preview_invoice_api_v1_invoices_preview_post) | **POST** /api/v1/invoices/preview | Preview Invoice |
| [**render_invoice_api_v1_invoices_invoice_id_renders_post**](InvoicesApi.md#render_invoice_api_v1_invoices_invoice_id_renders_post) | **POST** /api/v1/invoices/{invoice_id}/renders | Render Invoice |
| [**replace_invoice_api_v1_invoices_invoice_id_put**](InvoicesApi.md#replace_invoice_api_v1_invoices_invoice_id_put) | **PUT** /api/v1/invoices/{invoice_id} | Replace Invoice |
| [**restore_invoice_api_v1_invoices_invoice_id_restore_post**](InvoicesApi.md#restore_invoice_api_v1_invoices_invoice_id_restore_post) | **POST** /api/v1/invoices/{invoice_id}/restore | Restore Invoice |
| [**send_invoice_api_v1_invoices_invoice_id_send_post**](InvoicesApi.md#send_invoice_api_v1_invoices_invoice_id_send_post) | **POST** /api/v1/invoices/{invoice_id}/send | Send Invoice |
| [**validate_invoice_api_v1_invoices_validate_post**](InvoicesApi.md#validate_invoice_api_v1_invoices_validate_post) | **POST** /api/v1/invoices/validate | Validate Invoice |
| [**void_invoice_api_v1_invoices_invoice_id_void_post**](InvoicesApi.md#void_invoice_api_v1_invoices_invoice_id_void_post) | **POST** /api/v1/invoices/{invoice_id}/void | Void Invoice |


## archive_invoice_api_v1_invoices_invoice_id_archive_post

> <InvoiceResponse> archive_invoice_api_v1_invoices_invoice_id_archive_post(invoice_id)

Archive Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Archive Invoice
  result = api_instance.archive_invoice_api_v1_invoices_invoice_id_archive_post(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->archive_invoice_api_v1_invoices_invoice_id_archive_post: #{e}"
end
```

#### Using the archive_invoice_api_v1_invoices_invoice_id_archive_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> archive_invoice_api_v1_invoices_invoice_id_archive_post_with_http_info(invoice_id)

```ruby
begin
  # Archive Invoice
  data, status_code, headers = api_instance.archive_invoice_api_v1_invoices_invoice_id_archive_post_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->archive_invoice_api_v1_invoices_invoice_id_archive_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## calculate_invoice_api_v1_invoices_calculate_post

> Hash&lt;String, Object&gt; calculate_invoice_api_v1_invoices_calculate_post(invoice_draft_request)

Calculate Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_draft_request = InvoicePDFs::InvoiceDraftRequest.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', business_profile_id: 'bp_01ABC', customer_id: 'cus_01XYZ', line_items: [InvoicePDFs::InvoiceLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}) # InvoiceDraftRequest | 

begin
  # Calculate Invoice
  result = api_instance.calculate_invoice_api_v1_invoices_calculate_post(invoice_draft_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->calculate_invoice_api_v1_invoices_calculate_post: #{e}"
end
```

#### Using the calculate_invoice_api_v1_invoices_calculate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> calculate_invoice_api_v1_invoices_calculate_post_with_http_info(invoice_draft_request)

```ruby
begin
  # Calculate Invoice
  data, status_code, headers = api_instance.calculate_invoice_api_v1_invoices_calculate_post_with_http_info(invoice_draft_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->calculate_invoice_api_v1_invoices_calculate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_draft_request** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  |  |

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_invoice_api_v1_invoices_post

> <InvoiceResponse> create_invoice_api_v1_invoices_post(invoice_create_request, opts)

Create Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_create_request = InvoicePDFs::InvoiceCreateRequest.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', business_profile_id: 'bp_01ABC', customer_id: 'cus_01XYZ', line_items: [InvoicePDFs::InvoiceLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}) # InvoiceCreateRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Create Invoice
  result = api_instance.create_invoice_api_v1_invoices_post(invoice_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->create_invoice_api_v1_invoices_post: #{e}"
end
```

#### Using the create_invoice_api_v1_invoices_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> create_invoice_api_v1_invoices_post_with_http_info(invoice_create_request, opts)

```ruby
begin
  # Create Invoice
  data, status_code, headers = api_instance.create_invoice_api_v1_invoices_post_with_http_info(invoice_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->create_invoice_api_v1_invoices_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_create_request** | [**InvoiceCreateRequest**](InvoiceCreateRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_invoice_api_v1_invoices_invoice_id_delete

> <SimpleBoolResponse> delete_invoice_api_v1_invoices_invoice_id_delete(invoice_id)

Delete Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Delete Invoice
  result = api_instance.delete_invoice_api_v1_invoices_invoice_id_delete(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->delete_invoice_api_v1_invoices_invoice_id_delete: #{e}"
end
```

#### Using the delete_invoice_api_v1_invoices_invoice_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_invoice_api_v1_invoices_invoice_id_delete_with_http_info(invoice_id)

```ruby
begin
  # Delete Invoice
  data, status_code, headers = api_instance.delete_invoice_api_v1_invoices_invoice_id_delete_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->delete_invoice_api_v1_invoices_invoice_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post

> <InvoiceResponse> duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post(invoice_id)

Duplicate Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Duplicate Invoice
  result = api_instance.duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post: #{e}"
end
```

#### Using the duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post_with_http_info(invoice_id)

```ruby
begin
  # Duplicate Invoice
  data, status_code, headers = api_instance.duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->duplicate_invoice_api_v1_invoices_invoice_id_duplicate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## finalize_invoice_api_v1_invoices_invoice_id_finalize_post

> Hash&lt;String, Object&gt; finalize_invoice_api_v1_invoices_invoice_id_finalize_post(invoice_id, opts)

Finalize Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Finalize Invoice
  result = api_instance.finalize_invoice_api_v1_invoices_invoice_id_finalize_post(invoice_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->finalize_invoice_api_v1_invoices_invoice_id_finalize_post: #{e}"
end
```

#### Using the finalize_invoice_api_v1_invoices_invoice_id_finalize_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> finalize_invoice_api_v1_invoices_invoice_id_finalize_post_with_http_info(invoice_id, opts)

```ruby
begin
  # Finalize Invoice
  data, status_code, headers = api_instance.finalize_invoice_api_v1_invoices_invoice_id_finalize_post_with_http_info(invoice_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->finalize_invoice_api_v1_invoices_invoice_id_finalize_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_invoice_api_v1_invoices_invoice_id_get

> <InvoiceResponse> get_invoice_api_v1_invoices_invoice_id_get(invoice_id)

Get Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Get Invoice
  result = api_instance.get_invoice_api_v1_invoices_invoice_id_get(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->get_invoice_api_v1_invoices_invoice_id_get: #{e}"
end
```

#### Using the get_invoice_api_v1_invoices_invoice_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> get_invoice_api_v1_invoices_invoice_id_get_with_http_info(invoice_id)

```ruby
begin
  # Get Invoice
  data, status_code, headers = api_instance.get_invoice_api_v1_invoices_invoice_id_get_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->get_invoice_api_v1_invoices_invoice_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get

> <DeliveriesListResponse> list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get(invoice_id, opts)

List Invoice Deliveries

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Invoice Deliveries
  result = api_instance.list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get(invoice_id, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get: #{e}"
end
```

#### Using the list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveriesListResponse>, Integer, Hash)> list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get_with_http_info(invoice_id, opts)

```ruby
begin
  # List Invoice Deliveries
  data, status_code, headers = api_instance.list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get_with_http_info(invoice_id, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveriesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->list_invoice_deliveries_api_v1_invoices_invoice_id_deliveries_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**DeliveriesListResponse**](DeliveriesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_invoices_api_v1_invoices_get

> <InvoicesListResponse> list_invoices_api_v1_invoices_get(opts)

List Invoices

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example', # String | 
  status: 'status_example' # String | 
}

begin
  # List Invoices
  result = api_instance.list_invoices_api_v1_invoices_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->list_invoices_api_v1_invoices_get: #{e}"
end
```

#### Using the list_invoices_api_v1_invoices_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoicesListResponse>, Integer, Hash)> list_invoices_api_v1_invoices_get_with_http_info(opts)

```ruby
begin
  # List Invoices
  data, status_code, headers = api_instance.list_invoices_api_v1_invoices_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoicesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->list_invoices_api_v1_invoices_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |
| **status** | **String** |  | [optional] |

### Return type

[**InvoicesListResponse**](InvoicesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## mark_paid_api_v1_invoices_invoice_id_mark_paid_post

> <InvoiceResponse> mark_paid_api_v1_invoices_invoice_id_mark_paid_post(invoice_id)

Mark Paid

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Mark Paid
  result = api_instance.mark_paid_api_v1_invoices_invoice_id_mark_paid_post(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->mark_paid_api_v1_invoices_invoice_id_mark_paid_post: #{e}"
end
```

#### Using the mark_paid_api_v1_invoices_invoice_id_mark_paid_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> mark_paid_api_v1_invoices_invoice_id_mark_paid_post_with_http_info(invoice_id)

```ruby
begin
  # Mark Paid
  data, status_code, headers = api_instance.mark_paid_api_v1_invoices_invoice_id_mark_paid_post_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->mark_paid_api_v1_invoices_invoice_id_mark_paid_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## mark_sent_api_v1_invoices_invoice_id_mark_sent_post

> <InvoiceResponse> mark_sent_api_v1_invoices_invoice_id_mark_sent_post(invoice_id)

Mark Sent

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Mark Sent
  result = api_instance.mark_sent_api_v1_invoices_invoice_id_mark_sent_post(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->mark_sent_api_v1_invoices_invoice_id_mark_sent_post: #{e}"
end
```

#### Using the mark_sent_api_v1_invoices_invoice_id_mark_sent_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> mark_sent_api_v1_invoices_invoice_id_mark_sent_post_with_http_info(invoice_id)

```ruby
begin
  # Mark Sent
  data, status_code, headers = api_instance.mark_sent_api_v1_invoices_invoice_id_mark_sent_post_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->mark_sent_api_v1_invoices_invoice_id_mark_sent_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post

> <InvoiceResponse> mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post(invoice_id)

Mark Unpaid

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Mark Unpaid
  result = api_instance.mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post: #{e}"
end
```

#### Using the mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post_with_http_info(invoice_id)

```ruby
begin
  # Mark Unpaid
  data, status_code, headers = api_instance.mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->mark_unpaid_api_v1_invoices_invoice_id_mark_unpaid_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_invoice_api_v1_invoices_invoice_id_patch

> <InvoiceResponse> patch_invoice_api_v1_invoices_invoice_id_patch(invoice_id, invoice_patch_request, opts)

Patch Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 
invoice_patch_request = InvoicePDFs::InvoicePatchRequest.new # InvoicePatchRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Patch Invoice
  result = api_instance.patch_invoice_api_v1_invoices_invoice_id_patch(invoice_id, invoice_patch_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->patch_invoice_api_v1_invoices_invoice_id_patch: #{e}"
end
```

#### Using the patch_invoice_api_v1_invoices_invoice_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> patch_invoice_api_v1_invoices_invoice_id_patch_with_http_info(invoice_id, invoice_patch_request, opts)

```ruby
begin
  # Patch Invoice
  data, status_code, headers = api_instance.patch_invoice_api_v1_invoices_invoice_id_patch_with_http_info(invoice_id, invoice_patch_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->patch_invoice_api_v1_invoices_invoice_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **invoice_patch_request** | [**InvoicePatchRequest**](InvoicePatchRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## preview_invoice_api_v1_invoices_preview_post

> Object preview_invoice_api_v1_invoices_preview_post(invoice_preview_request)

Preview Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_preview_request = InvoicePDFs::InvoicePreviewRequest.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', business_profile_id: 'bp_01ABC', customer_id: 'cus_01XYZ', line_items: [InvoicePDFs::InvoiceLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}) # InvoicePreviewRequest | 

begin
  # Preview Invoice
  result = api_instance.preview_invoice_api_v1_invoices_preview_post(invoice_preview_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->preview_invoice_api_v1_invoices_preview_post: #{e}"
end
```

#### Using the preview_invoice_api_v1_invoices_preview_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> preview_invoice_api_v1_invoices_preview_post_with_http_info(invoice_preview_request)

```ruby
begin
  # Preview Invoice
  data, status_code, headers = api_instance.preview_invoice_api_v1_invoices_preview_post_with_http_info(invoice_preview_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->preview_invoice_api_v1_invoices_preview_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_preview_request** | [**InvoicePreviewRequest**](InvoicePreviewRequest.md) |  |  |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## render_invoice_api_v1_invoices_invoice_id_renders_post

> Object render_invoice_api_v1_invoices_invoice_id_renders_post(invoice_id, invoice_render_request, opts)

Render Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 
invoice_render_request = InvoicePDFs::InvoiceRenderRequest.new # InvoiceRenderRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Render Invoice
  result = api_instance.render_invoice_api_v1_invoices_invoice_id_renders_post(invoice_id, invoice_render_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->render_invoice_api_v1_invoices_invoice_id_renders_post: #{e}"
end
```

#### Using the render_invoice_api_v1_invoices_invoice_id_renders_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Object, Integer, Hash)> render_invoice_api_v1_invoices_invoice_id_renders_post_with_http_info(invoice_id, invoice_render_request, opts)

```ruby
begin
  # Render Invoice
  data, status_code, headers = api_instance.render_invoice_api_v1_invoices_invoice_id_renders_post_with_http_info(invoice_id, invoice_render_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Object
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->render_invoice_api_v1_invoices_invoice_id_renders_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **invoice_render_request** | [**InvoiceRenderRequest**](InvoiceRenderRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

**Object**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## replace_invoice_api_v1_invoices_invoice_id_put

> <InvoiceResponse> replace_invoice_api_v1_invoices_invoice_id_put(invoice_id, invoice_create_request, opts)

Replace Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 
invoice_create_request = InvoicePDFs::InvoiceCreateRequest.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', business_profile_id: 'bp_01ABC', customer_id: 'cus_01XYZ', line_items: [InvoicePDFs::InvoiceLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}) # InvoiceCreateRequest | 
opts = {
  idempotency_key: 'idempotency_key_example' # String | 
}

begin
  # Replace Invoice
  result = api_instance.replace_invoice_api_v1_invoices_invoice_id_put(invoice_id, invoice_create_request, opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->replace_invoice_api_v1_invoices_invoice_id_put: #{e}"
end
```

#### Using the replace_invoice_api_v1_invoices_invoice_id_put_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> replace_invoice_api_v1_invoices_invoice_id_put_with_http_info(invoice_id, invoice_create_request, opts)

```ruby
begin
  # Replace Invoice
  data, status_code, headers = api_instance.replace_invoice_api_v1_invoices_invoice_id_put_with_http_info(invoice_id, invoice_create_request, opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->replace_invoice_api_v1_invoices_invoice_id_put_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **invoice_create_request** | [**InvoiceCreateRequest**](InvoiceCreateRequest.md) |  |  |
| **idempotency_key** | **String** |  | [optional] |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## restore_invoice_api_v1_invoices_invoice_id_restore_post

> <InvoiceResponse> restore_invoice_api_v1_invoices_invoice_id_restore_post(invoice_id)

Restore Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Restore Invoice
  result = api_instance.restore_invoice_api_v1_invoices_invoice_id_restore_post(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->restore_invoice_api_v1_invoices_invoice_id_restore_post: #{e}"
end
```

#### Using the restore_invoice_api_v1_invoices_invoice_id_restore_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> restore_invoice_api_v1_invoices_invoice_id_restore_post_with_http_info(invoice_id)

```ruby
begin
  # Restore Invoice
  data, status_code, headers = api_instance.restore_invoice_api_v1_invoices_invoice_id_restore_post_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->restore_invoice_api_v1_invoices_invoice_id_restore_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## send_invoice_api_v1_invoices_invoice_id_send_post

> <DeliveryResponse> send_invoice_api_v1_invoices_invoice_id_send_post(invoice_id, delivery_send_request)

Send Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 
delivery_send_request = InvoicePDFs::DeliverySendRequest.new({to: ["client@example.com"]}) # DeliverySendRequest | 

begin
  # Send Invoice
  result = api_instance.send_invoice_api_v1_invoices_invoice_id_send_post(invoice_id, delivery_send_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->send_invoice_api_v1_invoices_invoice_id_send_post: #{e}"
end
```

#### Using the send_invoice_api_v1_invoices_invoice_id_send_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryResponse>, Integer, Hash)> send_invoice_api_v1_invoices_invoice_id_send_post_with_http_info(invoice_id, delivery_send_request)

```ruby
begin
  # Send Invoice
  data, status_code, headers = api_instance.send_invoice_api_v1_invoices_invoice_id_send_post_with_http_info(invoice_id, delivery_send_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->send_invoice_api_v1_invoices_invoice_id_send_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |
| **delivery_send_request** | [**DeliverySendRequest**](DeliverySendRequest.md) |  |  |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## validate_invoice_api_v1_invoices_validate_post

> Hash&lt;String, Object&gt; validate_invoice_api_v1_invoices_validate_post(invoice_draft_request)

Validate Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_draft_request = InvoicePDFs::InvoiceDraftRequest.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', business_profile_id: 'bp_01ABC', customer_id: 'cus_01XYZ', line_items: [InvoicePDFs::InvoiceLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}) # InvoiceDraftRequest | 

begin
  # Validate Invoice
  result = api_instance.validate_invoice_api_v1_invoices_validate_post(invoice_draft_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->validate_invoice_api_v1_invoices_validate_post: #{e}"
end
```

#### Using the validate_invoice_api_v1_invoices_validate_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> validate_invoice_api_v1_invoices_validate_post_with_http_info(invoice_draft_request)

```ruby
begin
  # Validate Invoice
  data, status_code, headers = api_instance.validate_invoice_api_v1_invoices_validate_post_with_http_info(invoice_draft_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->validate_invoice_api_v1_invoices_validate_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_draft_request** | [**InvoiceDraftRequest**](InvoiceDraftRequest.md) |  |  |

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## void_invoice_api_v1_invoices_invoice_id_void_post

> <InvoiceResponse> void_invoice_api_v1_invoices_invoice_id_void_post(invoice_id)

Void Invoice

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::InvoicesApi.new
invoice_id = 'invoice_id_example' # String | 

begin
  # Void Invoice
  result = api_instance.void_invoice_api_v1_invoices_invoice_id_void_post(invoice_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->void_invoice_api_v1_invoices_invoice_id_void_post: #{e}"
end
```

#### Using the void_invoice_api_v1_invoices_invoice_id_void_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<InvoiceResponse>, Integer, Hash)> void_invoice_api_v1_invoices_invoice_id_void_post_with_http_info(invoice_id)

```ruby
begin
  # Void Invoice
  data, status_code, headers = api_instance.void_invoice_api_v1_invoices_invoice_id_void_post_with_http_info(invoice_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <InvoiceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling InvoicesApi->void_invoice_api_v1_invoices_invoice_id_void_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **invoice_id** | **String** |  |  |

### Return type

[**InvoiceResponse**](InvoiceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

