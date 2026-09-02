# WWW::OpenAPIClient::SupplierInvoiceApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::SupplierInvoiceApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_supplier_invoice**](SupplierInvoiceApi.md#create_supplier_invoice) | **POST** /api/v1/supplier-invoices | 
[**delete_supplier_invoice**](SupplierInvoiceApi.md#delete_supplier_invoice) | **DELETE** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**get_supplier_invoice**](SupplierInvoiceApi.md#get_supplier_invoice) | **GET** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**list_supplier_invoices**](SupplierInvoiceApi.md#list_supplier_invoices) | **GET** /api/v1/supplier-invoices/ | 
[**update_supplier_invoice**](SupplierInvoiceApi.md#update_supplier_invoice) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**update_supplier_invoice_status**](SupplierInvoiceApi.md#update_supplier_invoice_status) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id}/status | 


# **create_supplier_invoice**
> SupplierInvoice create_supplier_invoice(supplier_invoice => $supplier_invoice)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierInvoiceApi;
my $api_instance = WWW::OpenAPIClient::SupplierInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_invoice = WWW::OpenAPIClient::Object::SupplierInvoice->new(); # SupplierInvoice | 

eval {
    my $result = $api_instance->create_supplier_invoice(supplier_invoice => $supplier_invoice);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierInvoiceApi->create_supplier_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_invoice** | [**SupplierInvoice**](SupplierInvoice.md)|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_supplier_invoice**
> delete_supplier_invoice(supplier_invoice_id => $supplier_invoice_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierInvoiceApi;
my $api_instance = WWW::OpenAPIClient::SupplierInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_invoice_id = "supplier_invoice_id_example"; # string | 

eval {
    $api_instance->delete_supplier_invoice(supplier_invoice_id => $supplier_invoice_id);
};
if ($@) {
    warn "Exception when calling SupplierInvoiceApi->delete_supplier_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_invoice_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_supplier_invoice**
> SupplierInvoice get_supplier_invoice(supplier_invoice_id => $supplier_invoice_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierInvoiceApi;
my $api_instance = WWW::OpenAPIClient::SupplierInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_invoice_id = "supplier_invoice_id_example"; # string | 

eval {
    my $result = $api_instance->get_supplier_invoice(supplier_invoice_id => $supplier_invoice_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierInvoiceApi->get_supplier_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_invoice_id** | **string**|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_supplier_invoices**
> ARRAY[SupplierInvoice] list_supplier_invoices(page => $page, page_size => $page_size, status => $status, purchase_order_id => $purchase_order_id, supplier_name => $supplier_name)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierInvoiceApi;
my $api_instance = WWW::OpenAPIClient::SupplierInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $purchase_order_id = "purchase_order_id_example"; # string | 
my $supplier_name = "supplier_name_example"; # string | 

eval {
    my $result = $api_instance->list_supplier_invoices(page => $page, page_size => $page_size, status => $status, purchase_order_id => $purchase_order_id, supplier_name => $supplier_name);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierInvoiceApi->list_supplier_invoices: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **purchase_order_id** | **string**|  | [optional] 
 **supplier_name** | **string**|  | [optional] 

### Return type

[**ARRAY[SupplierInvoice]**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_supplier_invoice**
> SupplierInvoice update_supplier_invoice(supplier_invoice_id => $supplier_invoice_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierInvoiceApi;
my $api_instance = WWW::OpenAPIClient::SupplierInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_invoice_id = "supplier_invoice_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_supplier_invoice(supplier_invoice_id => $supplier_invoice_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierInvoiceApi->update_supplier_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_invoice_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_supplier_invoice_status**
> SupplierInvoice update_supplier_invoice_status(supplier_invoice_id => $supplier_invoice_id, supplier_invoice_status_update => $supplier_invoice_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierInvoiceApi;
my $api_instance = WWW::OpenAPIClient::SupplierInvoiceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_invoice_id = "supplier_invoice_id_example"; # string | 
my $supplier_invoice_status_update = WWW::OpenAPIClient::Object::SupplierInvoiceStatusUpdate->new(); # SupplierInvoiceStatusUpdate | 

eval {
    my $result = $api_instance->update_supplier_invoice_status(supplier_invoice_id => $supplier_invoice_id, supplier_invoice_status_update => $supplier_invoice_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierInvoiceApi->update_supplier_invoice_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_invoice_id** | **string**|  | 
 **supplier_invoice_status_update** | [**SupplierInvoiceStatusUpdate**](SupplierInvoiceStatusUpdate.md)|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

