# InvoicePDFs::JobsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**cancel_job**](JobsApi.md#cancel_job) | **POST** /api/v1/jobs/{job_id}/cancel | Cancel Job |
| [**get_job**](JobsApi.md#get_job) | **GET** /api/v1/jobs/{job_id} | Get Job |
| [**list_jobs**](JobsApi.md#list_jobs) | **GET** /api/v1/jobs | List Jobs |
| [**retry_job**](JobsApi.md#retry_job) | **POST** /api/v1/jobs/{job_id}/retry | Retry Job |


## cancel_job

> <JobResponse> cancel_job(job_id)

Cancel Job

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::JobsApi.new
job_id = 'job_id_example' # String | 

begin
  # Cancel Job
  result = api_instance.cancel_job(job_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->cancel_job: #{e}"
end
```

#### Using the cancel_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobResponse>, Integer, Hash)> cancel_job_with_http_info(job_id)

```ruby
begin
  # Cancel Job
  data, status_code, headers = api_instance.cancel_job_with_http_info(job_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->cancel_job_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** |  |  |

### Return type

[**JobResponse**](JobResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## get_job

> <JobResponse> get_job(job_id)

Get Job

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::JobsApi.new
job_id = 'job_id_example' # String | 

begin
  # Get Job
  result = api_instance.get_job(job_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->get_job: #{e}"
end
```

#### Using the get_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobResponse>, Integer, Hash)> get_job_with_http_info(job_id)

```ruby
begin
  # Get Job
  data, status_code, headers = api_instance.get_job_with_http_info(job_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->get_job_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** |  |  |

### Return type

[**JobResponse**](JobResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## list_jobs

> <JobsListResponse> list_jobs(opts)

List Jobs

This account's jobs, newest first.  Without it the other three routes here were unreachable: a job id was never returned by anything, so there was no way to arrive at one.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::JobsApi.new
opts = {
  limit: 56, # Integer | 
  cursor: 'cursor_example' # String | 
}

begin
  # List Jobs
  result = api_instance.list_jobs(opts)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->list_jobs: #{e}"
end
```

#### Using the list_jobs_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobsListResponse>, Integer, Hash)> list_jobs_with_http_info(opts)

```ruby
begin
  # List Jobs
  data, status_code, headers = api_instance.list_jobs_with_http_info(opts)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobsListResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->list_jobs_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **limit** | **Integer** |  | [optional][default to 50] |
| **cursor** | **String** |  | [optional] |

### Return type

[**JobsListResponse**](JobsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json


## retry_job

> <JobResponse> retry_job(job_id)

Retry Job

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::JobsApi.new
job_id = 'job_id_example' # String | 

begin
  # Retry Job
  result = api_instance.retry_job(job_id)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->retry_job: #{e}"
end
```

#### Using the retry_job_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<JobResponse>, Integer, Hash)> retry_job_with_http_info(job_id)

```ruby
begin
  # Retry Job
  data, status_code, headers = api_instance.retry_job_with_http_info(job_id)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <JobResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling JobsApi->retry_job_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **job_id** | **String** |  |  |

### Return type

[**JobResponse**](JobResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

