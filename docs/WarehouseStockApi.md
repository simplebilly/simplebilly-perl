# WWW::OpenAPIClient::WarehouseStockApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::WarehouseStockApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_warehouse_stock**](WarehouseStockApi.md#create_warehouse_stock) | **POST** /api/v1/warehouses/{warehouse_id}/stock | 
[**delete_warehouse_stock**](WarehouseStockApi.md#delete_warehouse_stock) | **DELETE** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 
[**list_warehouse_stock**](WarehouseStockApi.md#list_warehouse_stock) | **GET** /api/v1/warehouses/{warehouse_id}/stock | 
[**update_warehouse_stock**](WarehouseStockApi.md#update_warehouse_stock) | **PUT** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 


# **create_warehouse_stock**
> WarehouseStock create_warehouse_stock(warehouse_id => $warehouse_id, stock_adjustment => $stock_adjustment)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseStockApi;
my $api_instance = WWW::OpenAPIClient::WarehouseStockApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse_id = "warehouse_id_example"; # string | 
my $stock_adjustment = WWW::OpenAPIClient::Object::StockAdjustment->new(); # StockAdjustment | 

eval {
    my $result = $api_instance->create_warehouse_stock(warehouse_id => $warehouse_id, stock_adjustment => $stock_adjustment);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WarehouseStockApi->create_warehouse_stock: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse_id** | **string**|  | 
 **stock_adjustment** | [**StockAdjustment**](StockAdjustment.md)|  | 

### Return type

[**WarehouseStock**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_warehouse_stock**
> delete_warehouse_stock(warehouse_id => $warehouse_id, product_id => $product_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseStockApi;
my $api_instance = WWW::OpenAPIClient::WarehouseStockApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse_id = "warehouse_id_example"; # string | 
my $product_id = "product_id_example"; # string | 

eval {
    $api_instance->delete_warehouse_stock(warehouse_id => $warehouse_id, product_id => $product_id);
};
if ($@) {
    warn "Exception when calling WarehouseStockApi->delete_warehouse_stock: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse_id** | **string**|  | 
 **product_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_warehouse_stock**
> ARRAY[WarehouseStock] list_warehouse_stock(warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseStockApi;
my $api_instance = WWW::OpenAPIClient::WarehouseStockApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse_id = "warehouse_id_example"; # string | 

eval {
    my $result = $api_instance->list_warehouse_stock(warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WarehouseStockApi->list_warehouse_stock: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse_id** | **string**|  | 

### Return type

[**ARRAY[WarehouseStock]**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_warehouse_stock**
> WarehouseStock update_warehouse_stock(warehouse_id => $warehouse_id, product_id => $product_id, stock_adjustment => $stock_adjustment)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseStockApi;
my $api_instance = WWW::OpenAPIClient::WarehouseStockApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse_id = "warehouse_id_example"; # string | 
my $product_id = "product_id_example"; # string | 
my $stock_adjustment = WWW::OpenAPIClient::Object::StockAdjustment->new(); # StockAdjustment | 

eval {
    my $result = $api_instance->update_warehouse_stock(warehouse_id => $warehouse_id, product_id => $product_id, stock_adjustment => $stock_adjustment);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WarehouseStockApi->update_warehouse_stock: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse_id** | **string**|  | 
 **product_id** | **string**|  | 
 **stock_adjustment** | [**StockAdjustment**](StockAdjustment.md)|  | 

### Return type

[**WarehouseStock**](WarehouseStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

