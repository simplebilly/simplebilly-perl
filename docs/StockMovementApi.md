# WWW::OpenAPIClient::StockMovementApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::StockMovementApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_stock_movement**](StockMovementApi.md#get_stock_movement) | **GET** /api/v1/stock-movements/{movement_id} | 
[**list_stock_movements**](StockMovementApi.md#list_stock_movements) | **GET** /api/v1/stock-movements/ | 


# **get_stock_movement**
> StockMovement get_stock_movement(movement_id => $movement_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StockMovementApi;
my $api_instance = WWW::OpenAPIClient::StockMovementApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $movement_id = "movement_id_example"; # string | 

eval {
    my $result = $api_instance->get_stock_movement(movement_id => $movement_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StockMovementApi->get_stock_movement: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **movement_id** | **string**|  | 

### Return type

[**StockMovement**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_stock_movements**
> ARRAY[StockMovement] list_stock_movements(page => $page, page_size => $page_size, product_id => $product_id, warehouse_id => $warehouse_id, movement_type => $movement_type, from => $from, to => $to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StockMovementApi;
my $api_instance = WWW::OpenAPIClient::StockMovementApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $product_id = "product_id_example"; # string | 
my $warehouse_id = "warehouse_id_example"; # string | 
my $movement_type = "movement_type_example"; # string | 
my $from = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only movements on or after this date (inclusive).
my $to = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only movements on or before this date (inclusive).

eval {
    my $result = $api_instance->list_stock_movements(page => $page, page_size => $page_size, product_id => $product_id, warehouse_id => $warehouse_id, movement_type => $movement_type, from => $from, to => $to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StockMovementApi->list_stock_movements: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **product_id** | **string**|  | [optional] 
 **warehouse_id** | **string**|  | [optional] 
 **movement_type** | **string**|  | [optional] 
 **from** | **DATE**| Only movements on or after this date (inclusive). | [optional] 
 **to** | **DATE**| Only movements on or before this date (inclusive). | [optional] 

### Return type

[**ARRAY[StockMovement]**](StockMovement.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

