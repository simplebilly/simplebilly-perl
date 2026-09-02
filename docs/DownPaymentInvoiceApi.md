# WWW::OpenAPIClient::DownPaymentInvoiceApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DownPaymentInvoiceApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**download_down_payment_invoice_pdf**](DownPaymentInvoiceApi.md#download_down_payment_invoice_pdf) | **GET** /api/v1/down-payment-invoices/{id}/pdf | 
[**get_down_payment_invoice**](DownPaymentInvoiceApi.md#get_down_payment_invoice) | **GET** /api/v1/down-payment-invoices/{id} | 
[**list_down_payment_invoices**](DownPaymentInvoiceApi.md#list_down_payment_invoices) | **GET** /api/v1/down-payment-invoices/ | 


# **download_down_payment_invoice_pdf**
> download_down_payment_invoice_pdf(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DownPaymentInvoiceApi;
my $api_instance = WWW::OpenAPIClient::DownPaymentInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->download_down_payment_invoice_pdf(id => $id);
};
if ($@) {
    warn "Exception when calling DownPaymentInvoiceApi->download_down_payment_invoice_pdf: $@\n";
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

# **get_down_payment_invoice**
> DownPaymentInvoice get_down_payment_invoice(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DownPaymentInvoiceApi;
my $api_instance = WWW::OpenAPIClient::DownPaymentInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_down_payment_invoice(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DownPaymentInvoiceApi->get_down_payment_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**DownPaymentInvoice**](DownPaymentInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_down_payment_invoices**
> ARRAY[DownPaymentInvoice] list_down_payment_invoices(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DownPaymentInvoiceApi;
my $api_instance = WWW::OpenAPIClient::DownPaymentInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->list_down_payment_invoices(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DownPaymentInvoiceApi->list_down_payment_invoices: $@\n";
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

[**ARRAY[DownPaymentInvoice]**](DownPaymentInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

