# InvoicePDFs::DeliveriesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**get_delivery**](DeliveriesApi.md#get_delivery) | **GET** /api/v1/deliveries/{delivery_id} | Get Delivery |
| [**retry_delivery**](DeliveriesApi.md#retry_delivery) | **POST** /api/v1/deliveries/{delivery_id}/retry | Retry Delivery |


## get_delivery

> <DeliveryResponse> get_delivery(delivery_id)

Get Delivery

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DeliveriesApi.new
delivery_id = 'delivery_id_example' # String | 

begin
  # Get Delivery
  result = api_instance.get_delivery(delivery_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DeliveriesApi->get_delivery: #{e}"
end
```

#### Using the get_delivery_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryResponse>, Integer, Hash)> get_delivery_with_http_info(delivery_id)

```ruby
begin
  # Get Delivery
  data, status_code, headers = api_instance.get_delivery_with_http_info(delivery_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DeliveriesApi->get_delivery_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_id** | **String** |  |  |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## retry_delivery

> <DeliveryResponse> retry_delivery(delivery_id)

Retry Delivery

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::DeliveriesApi.new
delivery_id = 'delivery_id_example' # String | 

begin
  # Retry Delivery
  result = api_instance.retry_delivery(delivery_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DeliveriesApi->retry_delivery: #{e}"
end
```

#### Using the retry_delivery_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DeliveryResponse>, Integer, Hash)> retry_delivery_with_http_info(delivery_id)

```ruby
begin
  # Retry Delivery
  data, status_code, headers = api_instance.retry_delivery_with_http_info(delivery_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling DeliveriesApi->retry_delivery_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_id** | **String** |  |  |

### Return type

[**DeliveryResponse**](DeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

