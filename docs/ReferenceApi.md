# InvoicePDFs::ReferenceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**list_countries**](ReferenceApi.md#list_countries) | **GET** /api/v1/reference/countries | List Countries |
| [**list_currencies**](ReferenceApi.md#list_currencies) | **GET** /api/v1/reference/currencies | List Currencies |
| [**list_document_types**](ReferenceApi.md#list_document_types) | **GET** /api/v1/reference/document-types | List Document Types |
| [**list_locales**](ReferenceApi.md#list_locales) | **GET** /api/v1/reference/locales | List Locales |
| [**list_page_sizes**](ReferenceApi.md#list_page_sizes) | **GET** /api/v1/reference/page-sizes | List Page Sizes |
| [**list_tax_categories**](ReferenceApi.md#list_tax_categories) | **GET** /api/v1/reference/tax-categories | List Tax Categories |
| [**list_tax_schemes**](ReferenceApi.md#list_tax_schemes) | **GET** /api/v1/reference/tax-schemes | List Tax Schemes |
| [**list_timezones**](ReferenceApi.md#list_timezones) | **GET** /api/v1/reference/timezones | List Timezones |
| [**list_unit_codes**](ReferenceApi.md#list_unit_codes) | **GET** /api/v1/reference/unit-codes | List Unit Codes |


## list_countries

> <CountriesListResponse> list_countries

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

> <Array(<CountriesListResponse>, Integer, Hash)> list_countries_with_http_info

```ruby
begin
  # List Countries
  data, status_code, headers = api_instance.list_countries_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CountriesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_countries_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CountriesListResponse**](CountriesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_currencies

> <CurrenciesListResponse> list_currencies

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

> <Array(<CurrenciesListResponse>, Integer, Hash)> list_currencies_with_http_info

```ruby
begin
  # List Currencies
  data, status_code, headers = api_instance.list_currencies_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CurrenciesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_currencies_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CurrenciesListResponse**](CurrenciesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_document_types

> <DocumentTypesListResponse> list_document_types

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

> <Array(<DocumentTypesListResponse>, Integer, Hash)> list_document_types_with_http_info

```ruby
begin
  # List Document Types
  data, status_code, headers = api_instance.list_document_types_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentTypesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_document_types_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**DocumentTypesListResponse**](DocumentTypesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_locales

> <LocalesListResponse> list_locales

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

> <Array(<LocalesListResponse>, Integer, Hash)> list_locales_with_http_info

```ruby
begin
  # List Locales
  data, status_code, headers = api_instance.list_locales_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <LocalesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_locales_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**LocalesListResponse**](LocalesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_page_sizes

> <PageSizesListResponse> list_page_sizes

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

> <Array(<PageSizesListResponse>, Integer, Hash)> list_page_sizes_with_http_info

```ruby
begin
  # List Page Sizes
  data, status_code, headers = api_instance.list_page_sizes_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <PageSizesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_page_sizes_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PageSizesListResponse**](PageSizesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_tax_categories

> <CodeListResponse> list_tax_categories

List Tax Categories

UNCL5305, in full — the VAT treatment of a line, which its rate does not say.  Two lines at 0% may be zero-rated, exempt, reverse-charge or outside scope, and EN 16931 puts them in separate VAT breakdown groups with different mandatory fields. Exhaustive: a category outside this list is wrong.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Tax Categories
  result = api_instance.list_tax_categories
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_tax_categories: #{e}"
end
```

#### Using the list_tax_categories_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CodeListResponse>, Integer, Hash)> list_tax_categories_with_http_info

```ruby
begin
  # List Tax Categories
  data, status_code, headers = api_instance.list_tax_categories_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CodeListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_tax_categories_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CodeListResponse**](CodeListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_tax_schemes

> <CodeListResponse> list_tax_schemes

List Tax Schemes

UNCL5153 — which tax regime a document is issued under, one per document.  `VAT` is the only member an e-invoice can carry; the others exist so a caller can state that their tax is *not* VAT and be told so, rather than have VAT assumed on their behalf. There is no default: a PDF does not need a scheme, and guessing one puts a claim in a document a tax authority reads that the caller never made.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Tax Schemes
  result = api_instance.list_tax_schemes
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_tax_schemes: #{e}"
end
```

#### Using the list_tax_schemes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CodeListResponse>, Integer, Hash)> list_tax_schemes_with_http_info

```ruby
begin
  # List Tax Schemes
  data, status_code, headers = api_instance.list_tax_schemes_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CodeListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_tax_schemes_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CodeListResponse**](CodeListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_timezones

> <TimezonesListResponse> list_timezones

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

> <Array(<TimezonesListResponse>, Integer, Hash)> list_timezones_with_http_info

```ruby
begin
  # List Timezones
  data, status_code, headers = api_instance.list_timezones_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <TimezonesListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_timezones_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**TimezonesListResponse**](TimezonesListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_unit_codes

> <CodeListResponse> list_unit_codes

List Unit Codes

UN/ECE Recommendation 20 — the unit a line item is measured in.  A **shortlist**: twenty-one of hundreds, ordered by how often an invoice needs them. `exhaustive` is false, and it means it — `unit_code` accepts any value, nothing validates against this list, and an uncommon code is still correct. Offered because the field takes a code rather than the printed label: mapping \"hrs\" to HUR is an inference that is right until it silently is not, and the audience for the result is a tax authority.

### Examples

```ruby
require 'time'
require 'invoicepdfs'

api_instance = InvoicePDFs::ReferenceApi.new

begin
  # List Unit Codes
  result = api_instance.list_unit_codes
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_unit_codes: #{e}"
end
```

#### Using the list_unit_codes_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<CodeListResponse>, Integer, Hash)> list_unit_codes_with_http_info

```ruby
begin
  # List Unit Codes
  data, status_code, headers = api_instance.list_unit_codes_with_http_info
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <CodeListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ReferenceApi->list_unit_codes_with_http_info: #{e}"
end
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**CodeListResponse**](CodeListResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

