# WWW::OpenAPIClient::StockTransferApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::StockTransferApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_stock_transfer**](StockTransferApi.md#create_stock_transfer) | **POST** /api/v1/stock-transfers | 
[**delete_stock_transfer**](StockTransferApi.md#delete_stock_transfer) | **DELETE** /api/v1/stock-transfers/{stock_transfer_id} | 
[**get_stock_transfer**](StockTransferApi.md#get_stock_transfer) | **GET** /api/v1/stock-transfers/{stock_transfer_id} | 
[**list_stock_transfers**](StockTransferApi.md#list_stock_transfers) | **GET** /api/v1/stock-transfers/ | 
[**update_stock_transfer_status**](StockTransferApi.md#update_stock_transfer_status) | **PUT** /api/v1/stock-transfers/{stock_transfer_id}/status | 


# **create_stock_transfer**
> StockTransfer create_stock_transfer(stock_transfer => $stock_transfer)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StockTransferApi;
my $api_instance = WWW::OpenAPIClient::StockTransferApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $stock_transfer = WWW::OpenAPIClient::Object::StockTransfer->new(); # StockTransfer | 

eval {
    my $result = $api_instance->create_stock_transfer(stock_transfer => $stock_transfer);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StockTransferApi->create_stock_transfer: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stock_transfer** | [**StockTransfer**](StockTransfer.md)|  | 

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_stock_transfer**
> delete_stock_transfer(stock_transfer_id => $stock_transfer_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StockTransferApi;
my $api_instance = WWW::OpenAPIClient::StockTransferApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $stock_transfer_id = "stock_transfer_id_example"; # string | 

eval {
    $api_instance->delete_stock_transfer(stock_transfer_id => $stock_transfer_id);
};
if ($@) {
    warn "Exception when calling StockTransferApi->delete_stock_transfer: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stock_transfer_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_stock_transfer**
> StockTransfer get_stock_transfer(stock_transfer_id => $stock_transfer_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StockTransferApi;
my $api_instance = WWW::OpenAPIClient::StockTransferApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $stock_transfer_id = "stock_transfer_id_example"; # string | 

eval {
    my $result = $api_instance->get_stock_transfer(stock_transfer_id => $stock_transfer_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StockTransferApi->get_stock_transfer: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stock_transfer_id** | **string**|  | 

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_stock_transfers**
> ARRAY[StockTransfer] list_stock_transfers(page => $page, page_size => $page_size, status => $status, warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StockTransferApi;
my $api_instance = WWW::OpenAPIClient::StockTransferApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $warehouse_id = "warehouse_id_example"; # string | 

eval {
    my $result = $api_instance->list_stock_transfers(page => $page, page_size => $page_size, status => $status, warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StockTransferApi->list_stock_transfers: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **warehouse_id** | **string**|  | [optional] 

### Return type

[**ARRAY[StockTransfer]**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_stock_transfer_status**
> StockTransfer update_stock_transfer_status(stock_transfer_id => $stock_transfer_id, stock_transfer_status_update => $stock_transfer_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StockTransferApi;
my $api_instance = WWW::OpenAPIClient::StockTransferApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $stock_transfer_id = "stock_transfer_id_example"; # string | 
my $stock_transfer_status_update = WWW::OpenAPIClient::Object::StockTransferStatusUpdate->new(); # StockTransferStatusUpdate | 

eval {
    my $result = $api_instance->update_stock_transfer_status(stock_transfer_id => $stock_transfer_id, stock_transfer_status_update => $stock_transfer_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StockTransferApi->update_stock_transfer_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **stock_transfer_id** | **string**|  | 
 **stock_transfer_status_update** | [**StockTransferStatusUpdate**](StockTransferStatusUpdate.md)|  | 

### Return type

[**StockTransfer**](StockTransfer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

