# InvoicePDFs::AuthApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**exchange_auth_token**](AuthApi.md#exchange_auth_token) | **POST** /api/v1/auth/token | Exchange Auth Token |
| [**get_current_user**](AuthApi.md#get_current_user) | **GET** /api/v1/auth/me | Get Current User |
| [**logout**](AuthApi.md#logout) | **POST** /api/v1/auth/logout | Logout |
| [**refresh_access_token**](AuthApi.md#refresh_access_token) | **POST** /api/v1/auth/refresh | Refresh Access Token |
| [**register**](AuthApi.md#register) | **POST** /api/v1/auth/register | Register |
| [**request_password_reset**](AuthApi.md#request_password_reset) | **POST** /api/v1/auth/forgot-password | Request Password Reset |
| [**reset_password**](AuthApi.md#reset_password) | **POST** /api/v1/auth/reset-password | Reset Password |
| [**update_current_user**](AuthApi.md#update_current_user) | **PATCH** /api/v1/auth/me | Update Current User |


## exchange_auth_token

> <AuthTokenResponse> exchange_auth_token(auth_token_request)

Exchange Auth Token

Exchange a Firebase ID token for account info.  Use this on login: the client authenticates with Firebase, sends the ID token here, and receives the InvoicePDFs account details. The Firebase token itself is used as the Bearer token for subsequent API calls.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_token_request = InvoicePDFs::AuthTokenRequest.new({id_token: 'id_token_example'}) # AuthTokenRequest | 

begin
  # Exchange Auth Token
  result = api_instance.exchange_auth_token(auth_token_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->exchange_auth_token: #{e}"
end
```

#### Using the exchange_auth_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthTokenResponse>, Integer, Hash)> exchange_auth_token_with_http_info(auth_token_request)

```ruby
begin
  # Exchange Auth Token
  data, status_code, headers = api_instance.exchange_auth_token_with_http_info(auth_token_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthTokenResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->exchange_auth_token_with_http_info: #{e}"
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


## get_current_user

> <AuthMeResponse> get_current_user

Get Current User

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
  # Get Current User
  result = api_instance.get_current_user
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->get_current_user: #{e}"
end
```

#### Using the get_current_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMeResponse>, Integer, Hash)> get_current_user_with_http_info

```ruby
begin
  # Get Current User
  data, status_code, headers = api_instance.get_current_user_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMeResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->get_current_user_with_http_info: #{e}"
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


## logout

> <AuthMessageResponse> logout

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
  result = api_instance.logout
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->logout: #{e}"
end
```

#### Using the logout_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMessageResponse>, Integer, Hash)> logout_with_http_info

```ruby
begin
  # Logout
  data, status_code, headers = api_instance.logout_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMessageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->logout_with_http_info: #{e}"
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


## refresh_access_token

> <AuthRefreshResponse> refresh_access_token(auth_refresh_request)

Refresh Access Token

Exchange a Firebase refresh token for a new ID token.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_refresh_request = InvoicePDFs::AuthRefreshRequest.new({refresh_token: 'refresh_token_example'}) # AuthRefreshRequest | 

begin
  # Refresh Access Token
  result = api_instance.refresh_access_token(auth_refresh_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->refresh_access_token: #{e}"
end
```

#### Using the refresh_access_token_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthRefreshResponse>, Integer, Hash)> refresh_access_token_with_http_info(auth_refresh_request)

```ruby
begin
  # Refresh Access Token
  data, status_code, headers = api_instance.refresh_access_token_with_http_info(auth_refresh_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthRefreshResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->refresh_access_token_with_http_info: #{e}"
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


## register

> <AuthRegisterResponse> register(auth_register_request)

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
  result = api_instance.register(auth_register_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->register: #{e}"
end
```

#### Using the register_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthRegisterResponse>, Integer, Hash)> register_with_http_info(auth_register_request)

```ruby
begin
  # Register
  data, status_code, headers = api_instance.register_with_http_info(auth_register_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthRegisterResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->register_with_http_info: #{e}"
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


## request_password_reset

> <AuthMessageResponse> request_password_reset(auth_forgot_password_request)

Request Password Reset

Send a password reset email via Firebase.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::AuthApi.new
auth_forgot_password_request = InvoicePDFs::AuthForgotPasswordRequest.new({email: 'email_example'}) # AuthForgotPasswordRequest | 

begin
  # Request Password Reset
  result = api_instance.request_password_reset(auth_forgot_password_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->request_password_reset: #{e}"
end
```

#### Using the request_password_reset_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMessageResponse>, Integer, Hash)> request_password_reset_with_http_info(auth_forgot_password_request)

```ruby
begin
  # Request Password Reset
  data, status_code, headers = api_instance.request_password_reset_with_http_info(auth_forgot_password_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMessageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->request_password_reset_with_http_info: #{e}"
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


## reset_password

> <AuthMessageResponse> reset_password(auth_reset_password_request)

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
  result = api_instance.reset_password(auth_reset_password_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->reset_password: #{e}"
end
```

#### Using the reset_password_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMessageResponse>, Integer, Hash)> reset_password_with_http_info(auth_reset_password_request)

```ruby
begin
  # Reset Password
  data, status_code, headers = api_instance.reset_password_with_http_info(auth_reset_password_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMessageResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->reset_password_with_http_info: #{e}"
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


## update_current_user

> <AuthMeResponse> update_current_user(auth_me_patch_request)

Update Current User

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
  # Update Current User
  result = api_instance.update_current_user(auth_me_patch_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->update_current_user: #{e}"
end
```

#### Using the update_current_user_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<AuthMeResponse>, Integer, Hash)> update_current_user_with_http_info(auth_me_patch_request)

```ruby
begin
  # Update Current User
  data, status_code, headers = api_instance.update_current_user_with_http_info(auth_me_patch_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <AuthMeResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling AuthApi->update_current_user_with_http_info: #{e}"
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

