# WWW::OpenAPIClient::InvoiceApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::InvoiceApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_invoice**](InvoiceApi.md#create_invoice) | **POST** /api/v1/invoices | 
[**delete_invoice**](InvoiceApi.md#delete_invoice) | **DELETE** /api/v1/invoices/{id} | 
[**download_invoice_pdf**](InvoiceApi.md#download_invoice_pdf) | **GET** /api/v1/invoices/{id}/pdf | 
[**get_invoice**](InvoiceApi.md#get_invoice) | **GET** /api/v1/invoices/{id} | 
[**get_invoice_pdf_url**](InvoiceApi.md#get_invoice_pdf_url) | **GET** /api/v1/invoices/{id}/pdf-url | 
[**get_invoices**](InvoiceApi.md#get_invoices) | **GET** /api/v1/invoices/ | 
[**invoice_restore**](InvoiceApi.md#invoice_restore) | **POST** /api/v1/invoices/{id}/restore | 
[**update_invoice**](InvoiceApi.md#update_invoice) | **PUT** /api/v1/invoices/{id} | 


# **create_invoice**
> Invoice create_invoice(invoice_create => $invoice_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $invoice_create = WWW::OpenAPIClient::Object::InvoiceCreate->new(); # InvoiceCreate | 

eval {
    my $result = $api_instance->create_invoice(invoice_create => $invoice_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InvoiceApi->create_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **invoice_create** | [**InvoiceCreate**](InvoiceCreate.md)|  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_invoice**
> delete_invoice(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_invoice(id => $id);
};
if ($@) {
    warn "Exception when calling InvoiceApi->delete_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_invoice_pdf**
> download_invoice_pdf(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->download_invoice_pdf(id => $id);
};
if ($@) {
    warn "Exception when calling InvoiceApi->download_invoice_pdf: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_invoice**
> Invoice get_invoice(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_invoice(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InvoiceApi->get_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_invoice_pdf_url**
> InvoicePdfUrlResponse get_invoice_pdf_url(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_invoice_pdf_url(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InvoiceApi->get_invoice_pdf_url: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**InvoicePdfUrlResponse**](InvoicePdfUrlResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_invoices**
> ARRAY[Invoice] get_invoices(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_invoices(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InvoiceApi->get_invoices: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **include_deleted** | **boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**ARRAY[Invoice]**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **invoice_restore**
> Invoice invoice_restore(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->invoice_restore(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InvoiceApi->invoice_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_invoice**
> Invoice update_invoice(id => $id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InvoiceApi;
my $api_instance = WWW::OpenAPIClient::InvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_invoice(id => $id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InvoiceApi->update_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

