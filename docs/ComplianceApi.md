# InvoicePDFs::ComplianceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
| ------ | ------------ | ----------- |
| [**download_document_xml**](ComplianceApi.md#download_document_xml) | **GET** /api/v1/documents/{document_id}/xml | Download Document Xml |
| [**render_document_xml**](ComplianceApi.md#render_document_xml) | **POST** /api/v1/documents/xml | Render Document Xml |
| [**validate_compliance**](ComplianceApi.md#validate_compliance) | **POST** /api/v1/documents/validate-compliance | Validate Compliance |


## download_document_xml

> String download_document_xml(document_id, profile)

Download Document Xml

The e-invoicing XML for a document already stored here.  Reads `data_json` directly rather than going through the render path's reconstruction: the status, the logo and the source document's number are all attached there for the *PDF*, and none of them belong in the XML. The credit note's BG-3 reference is already in the stored payload, resolved when the document was written.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ComplianceApi.new
document_id = 'document_id_example' # String | 
profile = 'peppol_bis_billing_3' # String | Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request.

begin
  # Download Document Xml
  result = api_instance.download_document_xml(document_id, profile)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ComplianceApi->download_document_xml: #{e}"
end
```

#### Using the download_document_xml_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(String, Integer, Hash)> download_document_xml_with_http_info(document_id, profile)

```ruby
begin
  # Download Document Xml
  data, status_code, headers = api_instance.download_document_xml_with_http_info(document_id, profile)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => String
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ComplianceApi->download_document_xml_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_id** | **String** |  |  |
| **profile** | **String** | Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request. |  |

### Return type

**String**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/xml, application/json


## render_document_xml

> String render_document_xml(document_compliance_request)

Render Document Xml

The e-invoicing XML for a document, without storing anything.  Takes the same body as `/validate-compliance`, and the pairing is the point: check first, then take the XML once it passes. Nothing here validates against the ruleset — a document missing mandatory fields serialises to XML missing those elements, which is a more useful artefact to look at than a refusal, and `/validate-compliance` is where the refusal belongs.  The syntax is not a parameter. It follows from the profile, because a profile already is a syntax plus a ruleset, and asking a caller for both is asking them to know that Peppol means UBL.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ComplianceApi.new
document_compliance_request = InvoicePDFs::DocumentComplianceRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}), profile: 'peppol_bis_billing_3'}) # DocumentComplianceRequest | 

begin
  # Render Document Xml
  result = api_instance.render_document_xml(document_compliance_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ComplianceApi->render_document_xml: #{e}"
end
```

#### Using the render_document_xml_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(String, Integer, Hash)> render_document_xml_with_http_info(document_compliance_request)

```ruby
begin
  # Render Document Xml
  data, status_code, headers = api_instance.render_document_xml_with_http_info(document_compliance_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => String
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ComplianceApi->render_document_xml_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_compliance_request** | [**DocumentComplianceRequest**](DocumentComplianceRequest.md) |  |  |

### Return type

**String**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/xml, application/json


## validate_compliance

> <DocumentComplianceResponse> validate_compliance(document_compliance_request)

Validate Compliance

Check a document against an e-invoicing ruleset without rendering it.  Costs no renders: nothing is stored and no PDF is produced, so a caller can check every invoice they are about to send rather than discovering the problem from a rejection weeks later.  Two tiers run, and both are reported. The mandatory-field check names a field of the request you can go and change. Schematron then serializes the document and runs the **published rules at a pinned version** over the result — the same artefacts an access point runs — so a finding here quotes the rule id a rejection notice would quote.  Read `valid` together with `fully_checked`: `valid` says nothing fatal was found, and `rulesets` says what actually ran to find it.

### Examples

```ruby
require 'time'
require 'invoicepdfs'
# setup authorization
InvoicePDFs.configure do |config|
  # Configure Bearer authorization: HTTPBearer
  config.access_token = 'YOUR_BEARER_TOKEN'
end

api_instance = InvoicePDFs::ComplianceApi.new
document_compliance_request = InvoicePDFs::DocumentComplianceRequest.new({data: InvoicePDFs::DocumentInvoiceDataInput.new({invoice_number: 'INV-2026-001', issue_date: Date.parse('Mon Jul 20 00:00:00 UTC 2026'), currency: 'USD', seller: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), buyer: InvoicePDFs::DocumentPartyInput.new({name: 'Acme Corp'}), line_items: [InvoicePDFs::DocumentLineItemInput.new({name: 'Web Development', quantity: '2', unit_price: '150.00'})]}), profile: 'peppol_bis_billing_3'}) # DocumentComplianceRequest | 

begin
  # Validate Compliance
  result = api_instance.validate_compliance(document_compliance_request)
  p result
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ComplianceApi->validate_compliance: #{e}"
end
```

#### Using the validate_compliance_with_http_info variant

This returns an Array which contains the response data, status code and headers.

> <Array(<DocumentComplianceResponse>, Integer, Hash)> validate_compliance_with_http_info(document_compliance_request)

```ruby
begin
  # Validate Compliance
  data, status_code, headers = api_instance.validate_compliance_with_http_info(document_compliance_request)
  p status_code # => 2xx
  p headers # => { ... }
  p data # => <DocumentComplianceResponse>
rescue InvoicePDFs::ApiError => e
  puts "Error when calling ComplianceApi->validate_compliance_with_http_info: #{e}"
end
```

### Parameters

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_compliance_request** | [**DocumentComplianceRequest**](DocumentComplianceRequest.md) |  |  |

### Return type

[**DocumentComplianceResponse**](DocumentComplianceResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

