# WWW::OpenAPIClient::GoodsReceiptApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GoodsReceiptApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_goods_receipt**](GoodsReceiptApi.md#create_goods_receipt) | **POST** /api/v1/goods-receipts | 
[**delete_goods_receipt**](GoodsReceiptApi.md#delete_goods_receipt) | **DELETE** /api/v1/goods-receipts/{goods_receipt_id} | 
[**get_goods_receipt**](GoodsReceiptApi.md#get_goods_receipt) | **GET** /api/v1/goods-receipts/{goods_receipt_id} | 
[**list_goods_receipts**](GoodsReceiptApi.md#list_goods_receipts) | **GET** /api/v1/goods-receipts/ | 


# **create_goods_receipt**
> GoodsReceipt create_goods_receipt(goods_receipt => $goods_receipt)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GoodsReceiptApi;
my $api_instance = WWW::OpenAPIClient::GoodsReceiptApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $goods_receipt = WWW::OpenAPIClient::Object::GoodsReceipt->new(); # GoodsReceipt | 

eval {
    my $result = $api_instance->create_goods_receipt(goods_receipt => $goods_receipt);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GoodsReceiptApi->create_goods_receipt: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **goods_receipt** | [**GoodsReceipt**](GoodsReceipt.md)|  | 

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_goods_receipt**
> delete_goods_receipt(goods_receipt_id => $goods_receipt_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GoodsReceiptApi;
my $api_instance = WWW::OpenAPIClient::GoodsReceiptApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $goods_receipt_id = "goods_receipt_id_example"; # string | 

eval {
    $api_instance->delete_goods_receipt(goods_receipt_id => $goods_receipt_id);
};
if ($@) {
    warn "Exception when calling GoodsReceiptApi->delete_goods_receipt: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **goods_receipt_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_goods_receipt**
> GoodsReceipt get_goods_receipt(goods_receipt_id => $goods_receipt_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GoodsReceiptApi;
my $api_instance = WWW::OpenAPIClient::GoodsReceiptApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $goods_receipt_id = "goods_receipt_id_example"; # string | 

eval {
    my $result = $api_instance->get_goods_receipt(goods_receipt_id => $goods_receipt_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GoodsReceiptApi->get_goods_receipt: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **goods_receipt_id** | **string**|  | 

### Return type

[**GoodsReceipt**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_goods_receipts**
> ARRAY[GoodsReceipt] list_goods_receipts(page => $page, page_size => $page_size, purchase_order_id => $purchase_order_id, supplier_name => $supplier_name, warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GoodsReceiptApi;
my $api_instance = WWW::OpenAPIClient::GoodsReceiptApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $purchase_order_id = "purchase_order_id_example"; # string | 
my $supplier_name = "supplier_name_example"; # string | 
my $warehouse_id = "warehouse_id_example"; # string | 

eval {
    my $result = $api_instance->list_goods_receipts(page => $page, page_size => $page_size, purchase_order_id => $purchase_order_id, supplier_name => $supplier_name, warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GoodsReceiptApi->list_goods_receipts: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **purchase_order_id** | **string**|  | [optional] 
 **supplier_name** | **string**|  | [optional] 
 **warehouse_id** | **string**|  | [optional] 

### Return type

[**ARRAY[GoodsReceipt]**](GoodsReceipt.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

