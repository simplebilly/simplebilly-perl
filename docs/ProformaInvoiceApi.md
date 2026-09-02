# WWW::OpenAPIClient::ProformaInvoiceApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ProformaInvoiceApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convert_proforma_to_invoice**](ProformaInvoiceApi.md#convert_proforma_to_invoice) | **POST** /api/v1/proforma-invoices/{proforma_id}/convert | 
[**create_proforma_invoice**](ProformaInvoiceApi.md#create_proforma_invoice) | **POST** /api/v1/proforma-invoices | 
[**delete_proforma_invoice**](ProformaInvoiceApi.md#delete_proforma_invoice) | **DELETE** /api/v1/proforma-invoices/{proforma_id} | 
[**get_proforma_invoice**](ProformaInvoiceApi.md#get_proforma_invoice) | **GET** /api/v1/proforma-invoices/{proforma_id} | 
[**list_proforma_invoices**](ProformaInvoiceApi.md#list_proforma_invoices) | **GET** /api/v1/proforma-invoices/ | 
[**update_proforma_invoice**](ProformaInvoiceApi.md#update_proforma_invoice) | **PUT** /api/v1/proforma-invoices/{proforma_id} | 


# **convert_proforma_to_invoice**
> ConvertResponse convert_proforma_to_invoice(proforma_id => $proforma_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProformaInvoiceApi;
my $api_instance = WWW::OpenAPIClient::ProformaInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $proforma_id = "proforma_id_example"; # string | 

eval {
    my $result = $api_instance->convert_proforma_to_invoice(proforma_id => $proforma_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProformaInvoiceApi->convert_proforma_to_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **proforma_id** | **string**|  | 

### Return type

[**ConvertResponse**](ConvertResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_proforma_invoice**
> ProformaInvoice create_proforma_invoice(proforma_invoice => $proforma_invoice)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProformaInvoiceApi;
my $api_instance = WWW::OpenAPIClient::ProformaInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $proforma_invoice = WWW::OpenAPIClient::Object::ProformaInvoice->new(); # ProformaInvoice | 

eval {
    my $result = $api_instance->create_proforma_invoice(proforma_invoice => $proforma_invoice);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProformaInvoiceApi->create_proforma_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **proforma_invoice** | [**ProformaInvoice**](ProformaInvoice.md)|  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_proforma_invoice**
> delete_proforma_invoice(proforma_id => $proforma_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProformaInvoiceApi;
my $api_instance = WWW::OpenAPIClient::ProformaInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $proforma_id = "proforma_id_example"; # string | 

eval {
    $api_instance->delete_proforma_invoice(proforma_id => $proforma_id);
};
if ($@) {
    warn "Exception when calling ProformaInvoiceApi->delete_proforma_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **proforma_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_proforma_invoice**
> ProformaInvoice get_proforma_invoice(proforma_id => $proforma_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProformaInvoiceApi;
my $api_instance = WWW::OpenAPIClient::ProformaInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $proforma_id = "proforma_id_example"; # string | 

eval {
    my $result = $api_instance->get_proforma_invoice(proforma_id => $proforma_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProformaInvoiceApi->get_proforma_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **proforma_id** | **string**|  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_proforma_invoices**
> ARRAY[ProformaInvoice] list_proforma_invoices(page => $page, page_size => $page_size, status => $status, customer_id => $customer_id, order_number => $order_number)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProformaInvoiceApi;
my $api_instance = WWW::OpenAPIClient::ProformaInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $customer_id = "customer_id_example"; # string | 
my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->list_proforma_invoices(page => $page, page_size => $page_size, status => $status, customer_id => $customer_id, order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProformaInvoiceApi->list_proforma_invoices: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **customer_id** | **string**|  | [optional] 
 **order_number** | **string**|  | [optional] 

### Return type

[**ARRAY[ProformaInvoice]**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_proforma_invoice**
> ProformaInvoice update_proforma_invoice(proforma_id => $proforma_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProformaInvoiceApi;
my $api_instance = WWW::OpenAPIClient::ProformaInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $proforma_id = "proforma_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_proforma_invoice(proforma_id => $proforma_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProformaInvoiceApi->update_proforma_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **proforma_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

