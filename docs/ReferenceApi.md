# InvoicePDFs::ReferenceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_countries**](ReferenceApi.md#list_countries) | **GET** /api/v1/reference/countries | List Countries |
| [**list_currencies**](ReferenceApi.md#list_currencies) | **GET** /api/v1/reference/currencies | List Currencies |
| [**list_document_types**](ReferenceApi.md#list_document_types) | **GET** /api/v1/reference/document-types | List Document Types |
| [**list_locales**](ReferenceApi.md#list_locales) | **GET** /api/v1/reference/locales | List Locales |
| [**list_page_sizes**](ReferenceApi.md#list_page_sizes) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**list_timezones**](ReferenceApi.md#list_timezones) | **GET** /api/v1/reference/timezones | List Timezones |


## list_countries

> Hash&lt;String, Object&gt; list_countries

List Countries

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Countries
  result = api_instance.list_countries
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_countries: #{e}"
end
```

#### Using the list_countries_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> list_countries_with_http_info

```ruby
begin
  # List Countries
  data, status_code, headers = api_instance.list_countries_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_countries_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_currencies

> Hash&lt;String, Object&gt; list_currencies

List Currencies

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Currencies
  result = api_instance.list_currencies
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_currencies: #{e}"
end
```

#### Using the list_currencies_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> list_currencies_with_http_info

```ruby
begin
  # List Currencies
  data, status_code, headers = api_instance.list_currencies_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_currencies_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_document_types

> Hash&lt;String, Object&gt; list_document_types

List Document Types

List every supported document type with the metadata a client needs to build a type-aware create form: the number prefix, whether it is payable / takes a source document / supports a reason, which line-item shape it uses (``standard`` = priced, ``shipped`` = quantities only), and the lifecycle actions available to it.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Document Types
  result = api_instance.list_document_types
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_document_types: #{e}"
end
```

#### Using the list_document_types_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> list_document_types_with_http_info

```ruby
begin
  # List Document Types
  data, status_code, headers = api_instance.list_document_types_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_document_types_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_locales

> Hash&lt;String, Object&gt; list_locales

List Locales

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Locales
  result = api_instance.list_locales
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_locales: #{e}"
end
```

#### Using the list_locales_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> list_locales_with_http_info

```ruby
begin
  # List Locales
  data, status_code, headers = api_instance.list_locales_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_locales_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_page_sizes

> Hash&lt;String, Object&gt; list_page_sizes

List Page Sizes

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Page Sizes
  result = api_instance.list_page_sizes
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_page_sizes: #{e}"
end
```

#### Using the list_page_sizes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> list_page_sizes_with_http_info

```ruby
begin
  # List Page Sizes
  data, status_code, headers = api_instance.list_page_sizes_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_page_sizes_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_timezones

> Hash&lt;String, Object&gt; list_timezones

List Timezones

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Timezones
  result = api_instance.list_timezones
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_timezones: #{e}"
end
```

#### Using the list_timezones_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(Hash&lt;String, Object&gt;, Integer, Hash)> list_timezones_with_http_info

```ruby
begin
  # List Timezones
  data, status_code, headers = api_instance.list_timezones_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => Hash&lt;String, Object&gt;
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_timezones_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

**Hash&lt;String, Object&gt;**

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

