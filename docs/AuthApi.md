# InvoicePDFs::AuthApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**forgot_password_api_v1_auth_forgot_password_post**](AuthApi.md#forgot_password_api_v1_auth_forgot_password_post) | **POST** /api/v1/auth/forgot-password | Forgot Password |
| [**logout_api_v1_auth_logout_post**](AuthApi.md#logout_api_v1_auth_logout_post) | **POST** /api/v1/auth/logout | Logout |
| [**me_api_v1_auth_me_get**](AuthApi.md#me_api_v1_auth_me_get) | **GET** /api/v1/auth/me | Me |
| [**patch_me_api_v1_auth_me_patch**](AuthApi.md#patch_me_api_v1_auth_me_patch) | **PATCH** /api/v1/auth/me | Patch Me |
| [**refresh_api_v1_auth_refresh_post**](AuthApi.md#refresh_api_v1_auth_refresh_post) | **POST** /api/v1/auth/refresh | Refresh |
| [**register_api_v1_auth_register_post**](AuthApi.md#register_api_v1_auth_register_post) | **POST** /api/v1/auth/register | Register |
| [**reset_password_api_v1_auth_reset_password_post**](AuthApi.md#reset_password_api_v1_auth_reset_password_post) | **POST** /api/v1/auth/reset-password | Reset Password |
| [**token_exchange_api_v1_auth_token_post**](AuthApi.md#token_exchange_api_v1_auth_token_post) | **POST** /api/v1/auth/token | Token Exchange |


## forgot_password_api_v1_auth_forgot_password_post

> <AuthMessageResponse> forgot_password_api_v1_auth_forgot_password_post(auth_forgot_password_request)

Forgot Password

Send a password reset email via Firebase.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_forgot_password_request = InvoicePDFs::AuthForgotPasswordRequest.new({email: 'email_example'}) # AuthForgotPasswordRequest | 

begin
  # Forgot Password
  result = api_instance.forgot_password_api_v1_auth_forgot_password_post(auth_forgot_password_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->forgot_password_api_v1_auth_forgot_password_post: #{e}"
end
```

#### Using the forgot_password_api_v1_auth_forgot_password_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMessageResponse>, Integer, Hash)> forgot_password_api_v1_auth_forgot_password_post_with_http_info(auth_forgot_password_request)

```ruby
begin
  # Forgot Password
  data, status_code, headers = api_instance.forgot_password_api_v1_auth_forgot_password_post_with_http_info(auth_forgot_password_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMessageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->forgot_password_api_v1_auth_forgot_password_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_forgot_password_request** | [**AuthForgotPasswordRequest**](AuthForgotPasswordRequest.md) |  |  |

### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## logout_api_v1_auth_logout_post

> <AuthMessageResponse> logout_api_v1_auth_logout_post

Logout

Revoke all Firebase refresh tokens for the authenticated user.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::AuthApi.new

begin
  # Logout
  result = api_instance.logout_api_v1_auth_logout_post
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->logout_api_v1_auth_logout_post: #{e}"
end
```

#### Using the logout_api_v1_auth_logout_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMessageResponse>, Integer, Hash)> logout_api_v1_auth_logout_post_with_http_info

```ruby
begin
  # Logout
  data, status_code, headers = api_instance.logout_api_v1_auth_logout_post_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMessageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->logout_api_v1_auth_logout_post_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## me_api_v1_auth_me_get

> <AuthMeResponse> me_api_v1_auth_me_get

Me

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::AuthApi.new

begin
  # Me
  result = api_instance.me_api_v1_auth_me_get
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->me_api_v1_auth_me_get: #{e}"
end
```

#### Using the me_api_v1_auth_me_get_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMeResponse>, Integer, Hash)> me_api_v1_auth_me_get_with_http_info

```ruby
begin
  # Me
  data, status_code, headers = api_instance.me_api_v1_auth_me_get_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMeResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->me_api_v1_auth_me_get_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**AuthMeResponse**](AuthMeResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## patch_me_api_v1_auth_me_patch

> <AuthMeResponse> patch_me_api_v1_auth_me_patch(auth_me_patch_request)

Patch Me

Update the authenticated account's name or email.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::AuthApi.new
auth_me_patch_request = InvoicePDFs::AuthMePatchRequest.new # AuthMePatchRequest | 

begin
  # Patch Me
  result = api_instance.patch_me_api_v1_auth_me_patch(auth_me_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->patch_me_api_v1_auth_me_patch: #{e}"
end
```

#### Using the patch_me_api_v1_auth_me_patch_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMeResponse>, Integer, Hash)> patch_me_api_v1_auth_me_patch_with_http_info(auth_me_patch_request)

```ruby
begin
  # Patch Me
  data, status_code, headers = api_instance.patch_me_api_v1_auth_me_patch_with_http_info(auth_me_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMeResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->patch_me_api_v1_auth_me_patch_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_me_patch_request** | [**AuthMePatchRequest**](AuthMePatchRequest.md) |  |  |

### Return type

[**AuthMeResponse**](AuthMeResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## refresh_api_v1_auth_refresh_post

> <AuthRefreshResponse> refresh_api_v1_auth_refresh_post(auth_refresh_request)

Refresh

Exchange a Firebase refresh token for a new ID token.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_refresh_request = InvoicePDFs::AuthRefreshRequest.new({refresh_token: 'refresh_token_example'}) # AuthRefreshRequest | 

begin
  # Refresh
  result = api_instance.refresh_api_v1_auth_refresh_post(auth_refresh_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->refresh_api_v1_auth_refresh_post: #{e}"
end
```

#### Using the refresh_api_v1_auth_refresh_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthRefreshResponse>, Integer, Hash)> refresh_api_v1_auth_refresh_post_with_http_info(auth_refresh_request)

```ruby
begin
  # Refresh
  data, status_code, headers = api_instance.refresh_api_v1_auth_refresh_post_with_http_info(auth_refresh_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthRefreshResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->refresh_api_v1_auth_refresh_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_refresh_request** | [**AuthRefreshRequest**](AuthRefreshRequest.md) |  |  |

### Return type

[**AuthRefreshResponse**](AuthRefreshResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## register_api_v1_auth_register_post

> <AuthRegisterResponse> register_api_v1_auth_register_post(auth_register_request)

Register

Register a new account using a Firebase ID token.  The client authenticates with Firebase (email/password, Google, etc.) and sends the resulting ID token here to create an InvoicePDFs account.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_register_request = InvoicePDFs::AuthRegisterRequest.new({id_token: 'id_token_example'}) # AuthRegisterRequest | 

begin
  # Register
  result = api_instance.register_api_v1_auth_register_post(auth_register_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->register_api_v1_auth_register_post: #{e}"
end
```

#### Using the register_api_v1_auth_register_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthRegisterResponse>, Integer, Hash)> register_api_v1_auth_register_post_with_http_info(auth_register_request)

```ruby
begin
  # Register
  data, status_code, headers = api_instance.register_api_v1_auth_register_post_with_http_info(auth_register_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthRegisterResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->register_api_v1_auth_register_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_register_request** | [**AuthRegisterRequest**](AuthRegisterRequest.md) |  |  |

### Return type

[**AuthRegisterResponse**](AuthRegisterResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## reset_password_api_v1_auth_reset_password_post

> <AuthMessageResponse> reset_password_api_v1_auth_reset_password_post(auth_reset_password_request)

Reset Password

Confirm a password reset using the code from the reset email.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_reset_password_request = InvoicePDFs::AuthResetPasswordRequest.new({oob_code: 'oob_code_example', new_password: 'new_password_example'}) # AuthResetPasswordRequest | 

begin
  # Reset Password
  result = api_instance.reset_password_api_v1_auth_reset_password_post(auth_reset_password_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->reset_password_api_v1_auth_reset_password_post: #{e}"
end
```

#### Using the reset_password_api_v1_auth_reset_password_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMessageResponse>, Integer, Hash)> reset_password_api_v1_auth_reset_password_post_with_http_info(auth_reset_password_request)

```ruby
begin
  # Reset Password
  data, status_code, headers = api_instance.reset_password_api_v1_auth_reset_password_post_with_http_info(auth_reset_password_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMessageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->reset_password_api_v1_auth_reset_password_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_reset_password_request** | [**AuthResetPasswordRequest**](AuthResetPasswordRequest.md) |  |  |

### Return type

[**AuthMessageResponse**](AuthMessageResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json


## token_exchange_api_v1_auth_token_post

> <AuthTokenResponse> token_exchange_api_v1_auth_token_post(auth_token_request)

Token Exchange

Exchange a Firebase ID token for account info.  Use this on login: the client authenticates with Firebase, sends the ID token here, and receives the InvoicePDFs account details. The Firebase token itself is used as the Bearer token for subsequent API calls.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_token_request = InvoicePDFs::AuthTokenRequest.new({id_token: 'id_token_example'}) # AuthTokenRequest | 

begin
  # Token Exchange
  result = api_instance.token_exchange_api_v1_auth_token_post(auth_token_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->token_exchange_api_v1_auth_token_post: #{e}"
end
```

#### Using the token_exchange_api_v1_auth_token_post_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthTokenResponse>, Integer, Hash)> token_exchange_api_v1_auth_token_post_with_http_info(auth_token_request)

```ruby
begin
  # Token Exchange
  data, status_code, headers = api_instance.token_exchange_api_v1_auth_token_post_with_http_info(auth_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthTokenResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->token_exchange_api_v1_auth_token_post_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **auth_token_request** | [**AuthTokenRequest**](AuthTokenRequest.md) |  |  |

### Return type

[**AuthTokenResponse**](AuthTokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

