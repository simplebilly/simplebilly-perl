# WWW::OpenAPIClient::PurchaseOrderApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PurchaseOrderApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_purchase_order**](PurchaseOrderApi.md#create_purchase_order) | **POST** /api/v1/purchase-orders | 
[**delete_purchase_order**](PurchaseOrderApi.md#delete_purchase_order) | **DELETE** /api/v1/purchase-orders/{purchase_order_id} | 
[**get_purchase_order**](PurchaseOrderApi.md#get_purchase_order) | **GET** /api/v1/purchase-orders/{purchase_order_id} | 
[**list_purchase_orders**](PurchaseOrderApi.md#list_purchase_orders) | **GET** /api/v1/purchase-orders/ | 
[**match_invoice**](PurchaseOrderApi.md#match_invoice) | **POST** /api/v1/purchase-orders/{purchase_order_id}/match-invoice | 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
[**update_purchase_order**](PurchaseOrderApi.md#update_purchase_order) | **PUT** /api/v1/purchase-orders/{purchase_order_id} | 
[**update_purchase_order_status**](PurchaseOrderApi.md#update_purchase_order_status) | **PUT** /api/v1/purchase-orders/{purchase_order_id}/status | 


# **create_purchase_order**
> PurchaseOrder create_purchase_order(purchase_order => $purchase_order)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PurchaseOrderApi;
my $api_instance = WWW::OpenAPIClient::PurchaseOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $purchase_order = WWW::OpenAPIClient::Object::PurchaseOrder->new(); # PurchaseOrder | 

eval {
    my $result = $api_instance->create_purchase_order(purchase_order => $purchase_order);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PurchaseOrderApi->create_purchase_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_order** | [**PurchaseOrder**](PurchaseOrder.md)|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_purchase_order**
> delete_purchase_order(purchase_order_id => $purchase_order_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PurchaseOrderApi;
my $api_instance = WWW::OpenAPIClient::PurchaseOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $purchase_order_id = "purchase_order_id_example"; # string | 

eval {
    $api_instance->delete_purchase_order(purchase_order_id => $purchase_order_id);
};
if ($@) {
    warn "Exception when calling PurchaseOrderApi->delete_purchase_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_order_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_purchase_order**
> PurchaseOrder get_purchase_order(purchase_order_id => $purchase_order_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PurchaseOrderApi;
my $api_instance = WWW::OpenAPIClient::PurchaseOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $purchase_order_id = "purchase_order_id_example"; # string | 

eval {
    my $result = $api_instance->get_purchase_order(purchase_order_id => $purchase_order_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PurchaseOrderApi->get_purchase_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_order_id** | **string**|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_purchase_orders**
> ARRAY[PurchaseOrder] list_purchase_orders(page => $page, page_size => $page_size, status => $status, supplier_name => $supplier_name, search => $search)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PurchaseOrderApi;
my $api_instance = WWW::OpenAPIClient::PurchaseOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $supplier_name = "supplier_name_example"; # string | 
my $search = "search_example"; # string | 

eval {
    my $result = $api_instance->list_purchase_orders(page => $page, page_size => $page_size, status => $status, supplier_name => $supplier_name, search => $search);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PurchaseOrderApi->list_purchase_orders: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **supplier_name** | **string**|  | [optional] 
 **search** | **string**|  | [optional] 

### Return type

[**ARRAY[PurchaseOrder]**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **match_invoice**
> object match_invoice(purchase_order_id => $purchase_order_id, invoice_match_request => $invoice_match_request)

3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PurchaseOrderApi;
my $api_instance = WWW::OpenAPIClient::PurchaseOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $purchase_order_id = "purchase_order_id_example"; # string | 
my $invoice_match_request = WWW::OpenAPIClient::Object::InvoiceMatchRequest->new(); # InvoiceMatchRequest | 

eval {
    my $result = $api_instance->match_invoice(purchase_order_id => $purchase_order_id, invoice_match_request => $invoice_match_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PurchaseOrderApi->match_invoice: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_order_id** | **string**|  | 
 **invoice_match_request** | [**InvoiceMatchRequest**](InvoiceMatchRequest.md)|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_purchase_order**
> PurchaseOrder update_purchase_order(purchase_order_id => $purchase_order_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PurchaseOrderApi;
my $api_instance = WWW::OpenAPIClient::PurchaseOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $purchase_order_id = "purchase_order_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_purchase_order(purchase_order_id => $purchase_order_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PurchaseOrderApi->update_purchase_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_order_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_purchase_order_status**
> PurchaseOrder update_purchase_order_status(purchase_order_id => $purchase_order_id, purchase_order_status_update => $purchase_order_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PurchaseOrderApi;
my $api_instance = WWW::OpenAPIClient::PurchaseOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $purchase_order_id = "purchase_order_id_example"; # string | 
my $purchase_order_status_update = WWW::OpenAPIClient::Object::PurchaseOrderStatusUpdate->new(); # PurchaseOrderStatusUpdate | 

eval {
    my $result = $api_instance->update_purchase_order_status(purchase_order_id => $purchase_order_id, purchase_order_status_update => $purchase_order_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PurchaseOrderApi->update_purchase_order_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **purchase_order_id** | **string**|  | 
 **purchase_order_status_update** | [**PurchaseOrderStatusUpdate**](PurchaseOrderStatusUpdate.md)|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

