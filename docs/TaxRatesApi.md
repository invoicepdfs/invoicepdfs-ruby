# InvoicePDFs::TaxRatesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_tax_rate_api_v1_tax_rates_post**](TaxRatesApi.md#create_tax_rate_api_v1_tax_rates_post) | **POST** /api/v1/tax-rates | Create Tax Rate |
| [**delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete**](TaxRatesApi.md#delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete) | **DELETE** /api/v1/tax-rates/{tax_rate_id} | Delete Tax Rate |
| [**get_tax_rate_api_v1_tax_rates_tax_rate_id_get**](TaxRatesApi.md#get_tax_rate_api_v1_tax_rates_tax_rate_id_get) | **GET** /api/v1/tax-rates/{tax_rate_id} | Get Tax Rate |
| [**list_tax_rates_api_v1_tax_rates_get**](TaxRatesApi.md#list_tax_rates_api_v1_tax_rates_get) | **GET** /api/v1/tax-rates | List Tax Rates |
| [**update_tax_rate_api_v1_tax_rates_tax_rate_id_patch**](TaxRatesApi.md#update_tax_rate_api_v1_tax_rates_tax_rate_id_patch) | **PATCH** /api/v1/tax-rates/{tax_rate_id} | Update Tax Rate |


## create_tax_rate_api_v1_tax_rates_post

> <TaxRateResponse> create_tax_rate_api_v1_tax_rates_post(tax_rate_create_request)

Create Tax Rate

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TaxRatesApi.new
tax_rate_create_request = InvoicePDFs::TaxRateCreateRequest.new({name: 'California sales tax', rate: '8.375'}) # TaxRateCreateRequest | 

begin
  # Create Tax Rate
  result = api_instance.create_tax_rate_api_v1_tax_rates_post(tax_rate_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->create_tax_rate_api_v1_tax_rates_post: #{e}"
end
```

#### Using the create_tax_rate_api_v1_tax_rates_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TaxRateResponse>, Integer, Hash)> create_tax_rate_api_v1_tax_rates_post_with_http_info(tax_rate_create_request)

```ruby
begin
  # Create Tax Rate
  data, status_code, headers = api_instance.create_tax_rate_api_v1_tax_rates_post_with_http_info(tax_rate_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TaxRateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->create_tax_rate_api_v1_tax_rates_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tax_rate_create_request** | [**TaxRateCreateRequest**](TaxRateCreateRequest.md) |  |  |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete

> <SimpleBoolResponse> delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete(tax_rate_id)

Delete Tax Rate

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TaxRatesApi.new
tax_rate_id = 'tax_rate_id_example' # String | 

begin
  # Delete Tax Rate
  result = api_instance.delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete(tax_rate_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete: #{e}"
end
```

#### Using the delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete_with_http_info(tax_rate_id)

```ruby
begin
  # Delete Tax Rate
  data, status_code, headers = api_instance.delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete_with_http_info(tax_rate_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->delete_tax_rate_api_v1_tax_rates_tax_rate_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tax_rate_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_tax_rate_api_v1_tax_rates_tax_rate_id_get

> <TaxRateResponse> get_tax_rate_api_v1_tax_rates_tax_rate_id_get(tax_rate_id)

Get Tax Rate

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TaxRatesApi.new
tax_rate_id = 'tax_rate_id_example' # String | 

begin
  # Get Tax Rate
  result = api_instance.get_tax_rate_api_v1_tax_rates_tax_rate_id_get(tax_rate_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->get_tax_rate_api_v1_tax_rates_tax_rate_id_get: #{e}"
end
```

#### Using the get_tax_rate_api_v1_tax_rates_tax_rate_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TaxRateResponse>, Integer, Hash)> get_tax_rate_api_v1_tax_rates_tax_rate_id_get_with_http_info(tax_rate_id)

```ruby
begin
  # Get Tax Rate
  data, status_code, headers = api_instance.get_tax_rate_api_v1_tax_rates_tax_rate_id_get_with_http_info(tax_rate_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TaxRateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->get_tax_rate_api_v1_tax_rates_tax_rate_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tax_rate_id** | **String** |  |  |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_tax_rates_api_v1_tax_rates_get

> <TaxRatesListResponse> list_tax_rates_api_v1_tax_rates_get(opts)

List Tax Rates

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TaxRatesApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Tax Rates
  result = api_instance.list_tax_rates_api_v1_tax_rates_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->list_tax_rates_api_v1_tax_rates_get: #{e}"
end
```

#### Using the list_tax_rates_api_v1_tax_rates_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TaxRatesListResponse>, Integer, Hash)> list_tax_rates_api_v1_tax_rates_get_with_http_info(opts)

```ruby
begin
  # List Tax Rates
  data, status_code, headers = api_instance.list_tax_rates_api_v1_tax_rates_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TaxRatesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->list_tax_rates_api_v1_tax_rates_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**TaxRatesListResponse**](TaxRatesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_tax_rate_api_v1_tax_rates_tax_rate_id_patch

> <TaxRateResponse> update_tax_rate_api_v1_tax_rates_tax_rate_id_patch(tax_rate_id, tax_rate_patch_request)

Update Tax Rate

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::TaxRatesApi.new
tax_rate_id = 'tax_rate_id_example' # String | 
tax_rate_patch_request = InvoicePDFs::TaxRatePatchRequest.new # TaxRatePatchRequest | 

begin
  # Update Tax Rate
  result = api_instance.update_tax_rate_api_v1_tax_rates_tax_rate_id_patch(tax_rate_id, tax_rate_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->update_tax_rate_api_v1_tax_rates_tax_rate_id_patch: #{e}"
end
```

#### Using the update_tax_rate_api_v1_tax_rates_tax_rate_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<TaxRateResponse>, Integer, Hash)> update_tax_rate_api_v1_tax_rates_tax_rate_id_patch_with_http_info(tax_rate_id, tax_rate_patch_request)

```ruby
begin
  # Update Tax Rate
  data, status_code, headers = api_instance.update_tax_rate_api_v1_tax_rates_tax_rate_id_patch_with_http_info(tax_rate_id, tax_rate_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TaxRateResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling TaxRatesApi->update_tax_rate_api_v1_tax_rates_tax_rate_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **tax_rate_id** | **String** |  |  |
| **tax_rate_patch_request** | [**TaxRatePatchRequest**](TaxRatePatchRequest.md) |  |  |

### Return type

[**TaxRateResponse**](TaxRateResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

