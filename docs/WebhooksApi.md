# InvoicePDFs::WebhooksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_webhook_endpoint_api_v1_webhook_endpoints_post**](WebhooksApi.md#create_webhook_endpoint_api_v1_webhook_endpoints_post) | **POST** /api/v1/webhook-endpoints | Create Webhook Endpoint |
| [**delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete**](WebhooksApi.md#delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete) | **DELETE** /api/v1/webhook-endpoints/{endpoint_id} | Delete Webhook Endpoint |
| [**get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get**](WebhooksApi.md#get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get) | **GET** /api/v1/webhook-deliveries/{delivery_id} | Get Webhook Delivery |
| [**get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get**](WebhooksApi.md#get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get) | **GET** /api/v1/webhook-endpoints/{endpoint_id} | Get Webhook Endpoint |
| [**list_webhook_deliveries_api_v1_webhook_deliveries_get**](WebhooksApi.md#list_webhook_deliveries_api_v1_webhook_deliveries_get) | **GET** /api/v1/webhook-deliveries | List Webhook Deliveries |
| [**list_webhook_endpoints_api_v1_webhook_endpoints_get**](WebhooksApi.md#list_webhook_endpoints_api_v1_webhook_endpoints_get) | **GET** /api/v1/webhook-endpoints | List Webhook Endpoints |
| [**retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post**](WebhooksApi.md#retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post) | **POST** /api/v1/webhook-deliveries/{delivery_id}/retry | Retry Webhook Delivery |
| [**rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post**](WebhooksApi.md#rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/rotate-secret | Rotate Webhook Secret |
| [**test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post**](WebhooksApi.md#test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/test | Test Webhook Endpoint |
| [**update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch**](WebhooksApi.md#update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch) | **PATCH** /api/v1/webhook-endpoints/{endpoint_id} | Update Webhook Endpoint |


## create_webhook_endpoint_api_v1_webhook_endpoints_post

> <WebhookEndpointResponse> create_webhook_endpoint_api_v1_webhook_endpoints_post(webhook_endpoint_create_request)

Create Webhook Endpoint

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
webhook_endpoint_create_request = InvoicePDFs::WebhookEndpointCreateRequest.new({url: 'https://example.com/webhooks', events: ["invoice.created", "invoice.paid"]}) # WebhookEndpointCreateRequest | 

begin
  # Create Webhook Endpoint
  result = api_instance.create_webhook_endpoint_api_v1_webhook_endpoints_post(webhook_endpoint_create_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->create_webhook_endpoint_api_v1_webhook_endpoints_post: #{e}"
end
```

#### Using the create_webhook_endpoint_api_v1_webhook_endpoints_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointResponse>, Integer, Hash)> create_webhook_endpoint_api_v1_webhook_endpoints_post_with_http_info(webhook_endpoint_create_request)

```ruby
begin
  # Create Webhook Endpoint
  data, status_code, headers = api_instance.create_webhook_endpoint_api_v1_webhook_endpoints_post_with_http_info(webhook_endpoint_create_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->create_webhook_endpoint_api_v1_webhook_endpoints_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **webhook_endpoint_create_request** | [**WebhookEndpointCreateRequest**](WebhookEndpointCreateRequest.md) |  |  |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete

> <SimpleBoolResponse> delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete(endpoint_id)

Delete Webhook Endpoint

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
endpoint_id = 'endpoint_id_example' # String | 

begin
  # Delete Webhook Endpoint
  result = api_instance.delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete(endpoint_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete: #{e}"
end
```

#### Using the delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<SimpleBoolResponse>, Integer, Hash)> delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete_with_http_info(endpoint_id)

```ruby
begin
  # Delete Webhook Endpoint
  data, status_code, headers = api_instance.delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete_with_http_info(endpoint_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <SimpleBoolResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->delete_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_delete_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get

> <WebhookDeliveryResponse> get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get(delivery_id)

Get Webhook Delivery

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
delivery_id = 'delivery_id_example' # String | 

begin
  # Get Webhook Delivery
  result = api_instance.get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get(delivery_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get: #{e}"
end
```

#### Using the get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookDeliveryResponse>, Integer, Hash)> get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get_with_http_info(delivery_id)

```ruby
begin
  # Get Webhook Delivery
  data, status_code, headers = api_instance.get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get_with_http_info(delivery_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookDeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_delivery_api_v1_webhook_deliveries_delivery_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_id** | **String** |  |  |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get

> <WebhookEndpointResponse> get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get(endpoint_id)

Get Webhook Endpoint

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
endpoint_id = 'endpoint_id_example' # String | 

begin
  # Get Webhook Endpoint
  result = api_instance.get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get(endpoint_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get: #{e}"
end
```

#### Using the get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointResponse>, Integer, Hash)> get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get_with_http_info(endpoint_id)

```ruby
begin
  # Get Webhook Endpoint
  data, status_code, headers = api_instance.get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get_with_http_info(endpoint_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->get_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_webhook_deliveries_api_v1_webhook_deliveries_get

> <WebhookDeliveriesListResponse> list_webhook_deliveries_api_v1_webhook_deliveries_get(opts)

List Webhook Deliveries

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Webhook Deliveries
  result = api_instance.list_webhook_deliveries_api_v1_webhook_deliveries_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->list_webhook_deliveries_api_v1_webhook_deliveries_get: #{e}"
end
```

#### Using the list_webhook_deliveries_api_v1_webhook_deliveries_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookDeliveriesListResponse>, Integer, Hash)> list_webhook_deliveries_api_v1_webhook_deliveries_get_with_http_info(opts)

```ruby
begin
  # List Webhook Deliveries
  data, status_code, headers = api_instance.list_webhook_deliveries_api_v1_webhook_deliveries_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookDeliveriesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->list_webhook_deliveries_api_v1_webhook_deliveries_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**WebhookDeliveriesListResponse**](WebhookDeliveriesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_webhook_endpoints_api_v1_webhook_endpoints_get

> <WebhookEndpointsListResponse> list_webhook_endpoints_api_v1_webhook_endpoints_get(opts)

List Webhook Endpoints

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Webhook Endpoints
  result = api_instance.list_webhook_endpoints_api_v1_webhook_endpoints_get(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->list_webhook_endpoints_api_v1_webhook_endpoints_get: #{e}"
end
```

#### Using the list_webhook_endpoints_api_v1_webhook_endpoints_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointsListResponse>, Integer, Hash)> list_webhook_endpoints_api_v1_webhook_endpoints_get_with_http_info(opts)

```ruby
begin
  # List Webhook Endpoints
  data, status_code, headers = api_instance.list_webhook_endpoints_api_v1_webhook_endpoints_get_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->list_webhook_endpoints_api_v1_webhook_endpoints_get_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**WebhookEndpointsListResponse**](WebhookEndpointsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post

> <WebhookDeliveryResponse> retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post(delivery_id)

Retry Webhook Delivery

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
delivery_id = 'delivery_id_example' # String | 

begin
  # Retry Webhook Delivery
  result = api_instance.retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post(delivery_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post: #{e}"
end
```

#### Using the retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookDeliveryResponse>, Integer, Hash)> retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post_with_http_info(delivery_id)

```ruby
begin
  # Retry Webhook Delivery
  data, status_code, headers = api_instance.retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post_with_http_info(delivery_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookDeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->retry_webhook_delivery_api_v1_webhook_deliveries_delivery_id_retry_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **delivery_id** | **String** |  |  |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post

> <WebhookSecretResponse> rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post(endpoint_id)

Rotate Webhook Secret

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
endpoint_id = 'endpoint_id_example' # String | 

begin
  # Rotate Webhook Secret
  result = api_instance.rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post(endpoint_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post: #{e}"
end
```

#### Using the rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookSecretResponse>, Integer, Hash)> rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post_with_http_info(endpoint_id)

```ruby
begin
  # Rotate Webhook Secret
  data, status_code, headers = api_instance.rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post_with_http_info(endpoint_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookSecretResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->rotate_webhook_secret_api_v1_webhook_endpoints_endpoint_id_rotate_secret_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |

### Return type

[**WebhookSecretResponse**](WebhookSecretResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post

> <WebhookDeliveryResponse> test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post(endpoint_id)

Test Webhook Endpoint

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
endpoint_id = 'endpoint_id_example' # String | 

begin
  # Test Webhook Endpoint
  result = api_instance.test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post(endpoint_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post: #{e}"
end
```

#### Using the test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookDeliveryResponse>, Integer, Hash)> test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post_with_http_info(endpoint_id)

```ruby
begin
  # Test Webhook Endpoint
  data, status_code, headers = api_instance.test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post_with_http_info(endpoint_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookDeliveryResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->test_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_test_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch

> <WebhookEndpointResponse> update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch(endpoint_id, webhook_endpoint_patch_request)

Update Webhook Endpoint

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::WebhooksApi.new
endpoint_id = 'endpoint_id_example' # String | 
webhook_endpoint_patch_request = InvoicePDFs::WebhookEndpointPatchRequest.new # WebhookEndpointPatchRequest | 

begin
  # Update Webhook Endpoint
  result = api_instance.update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch(endpoint_id, webhook_endpoint_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch: #{e}"
end
```

#### Using the update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<WebhookEndpointResponse>, Integer, Hash)> update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch_with_http_info(endpoint_id, webhook_endpoint_patch_request)

```ruby
begin
  # Update Webhook Endpoint
  data, status_code, headers = api_instance.update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch_with_http_info(endpoint_id, webhook_endpoint_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <WebhookEndpointResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling WebhooksApi->update_webhook_endpoint_api_v1_webhook_endpoints_endpoint_id_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **endpoint_id** | **String** |  |  |
| **webhook_endpoint_patch_request** | [**WebhookEndpointPatchRequest**](WebhookEndpointPatchRequest.md) |  |  |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

