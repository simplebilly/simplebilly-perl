# WWW::OpenAPIClient::InventoryValueApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::InventoryValueApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_inventory_value_api**](InventoryValueApi.md#get_inventory_value_api) | **GET** /api/v1/bookkeeping/inventory-value | 
[**record_inventory_value_api**](InventoryValueApi.md#record_inventory_value_api) | **POST** /api/v1/bookkeeping/inventory-value/record | 


# **get_inventory_value_api**
> CurrentInventoryValue get_inventory_value_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryValueApi;
my $api_instance = WWW::OpenAPIClient::InventoryValueApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_inventory_value_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryValueApi->get_inventory_value_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CurrentInventoryValue**](CurrentInventoryValue.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **record_inventory_value_api**
> InventoryValuePoint record_inventory_value_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryValueApi;
my $api_instance = WWW::OpenAPIClient::InventoryValueApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->record_inventory_value_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryValueApi->record_inventory_value_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InventoryValuePoint**](InventoryValuePoint.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

