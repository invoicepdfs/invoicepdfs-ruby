# InvoicePDFs::BillingApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**create_checkout_session**](BillingApi.md#create_checkout_session) | **POST** /api/v1/billing/checkout-session | Create Checkout Session |
| [**create_portal_session**](BillingApi.md#create_portal_session) | **POST** /api/v1/billing/portal-session | Create Portal Session |
| [**get_subscription**](BillingApi.md#get_subscription) | **GET** /api/v1/billing/subscription | Get Subscription |
| [**list_plans**](BillingApi.md#list_plans) | **GET** /api/v1/billing/plans | List Plans |


## create_checkout_session

> <BillingCheckoutResponse> create_checkout_session(billing_checkout_request)

Create Checkout Session

Create a Stripe Checkout session for a subscription.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BillingApi.new
billing_checkout_request = InvoicePDFs::BillingCheckoutRequest.new({price_id: 'price_id_example'}) # BillingCheckoutRequest | 

begin
  # Create Checkout Session
  result = api_instance.create_checkout_session(billing_checkout_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->create_checkout_session: #{e}"
end
```

#### Using the create_checkout_session_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BillingCheckoutResponse>, Integer, Hash)> create_checkout_session_with_http_info(billing_checkout_request)

```ruby
begin
  # Create Checkout Session
  data, status_code, headers = api_instance.create_checkout_session_with_http_info(billing_checkout_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BillingCheckoutResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->create_checkout_session_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **billing_checkout_request** | [**BillingCheckoutRequest**](BillingCheckoutRequest.md) |  |  |

### Return type

[**BillingCheckoutResponse**](BillingCheckoutResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## create_portal_session

> <BillingPortalResponse> create_portal_session

Create Portal Session

Create a Stripe Customer Portal session for self-service management.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BillingApi.new

begin
  # Create Portal Session
  result = api_instance.create_portal_session
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->create_portal_session: #{e}"
end
```

#### Using the create_portal_session_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BillingPortalResponse>, Integer, Hash)> create_portal_session_with_http_info

```ruby
begin
  # Create Portal Session
  data, status_code, headers = api_instance.create_portal_session_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BillingPortalResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->create_portal_session_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BillingPortalResponse**](BillingPortalResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_subscription

> <BillingSubscriptionResponse> get_subscription

Get Subscription

Get current subscription status (from DB, no Stripe API call).

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BillingApi.new

begin
  # Get Subscription
  result = api_instance.get_subscription
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->get_subscription: #{e}"
end
```

#### Using the get_subscription_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BillingSubscriptionResponse>, Integer, Hash)> get_subscription_with_http_info

```ruby
begin
  # Get Subscription
  data, status_code, headers = api_instance.get_subscription_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BillingSubscriptionResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->get_subscription_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BillingSubscriptionResponse**](BillingSubscriptionResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_plans

> <BillingPlansListResponse> list_plans

List Plans

Purchasable plans — the ones wired to a Stripe price.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::BillingApi.new

begin
  # List Plans
  result = api_instance.list_plans
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->list_plans: #{e}"
end
```

#### Using the list_plans_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<BillingPlansListResponse>, Integer, Hash)> list_plans_with_http_info

```ruby
begin
  # List Plans
  data, status_code, headers = api_instance.list_plans_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <BillingPlansListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling BillingApi->list_plans_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**BillingPlansListResponse**](BillingPlansListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

