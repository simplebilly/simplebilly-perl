# WWW::OpenAPIClient::WarehouseApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::WarehouseApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_warehouse**](WarehouseApi.md#create_warehouse) | **POST** /api/v1/warehouses | 
[**delete_warehouse**](WarehouseApi.md#delete_warehouse) | **DELETE** /api/v1/warehouses/{warehouse_id} | 
[**get_warehouse**](WarehouseApi.md#get_warehouse) | **GET** /api/v1/warehouses/{warehouse_id} | 
[**list_warehouses**](WarehouseApi.md#list_warehouses) | **GET** /api/v1/warehouses/ | 
[**update_warehouse**](WarehouseApi.md#update_warehouse) | **PUT** /api/v1/warehouses/{warehouse_id} | 


# **create_warehouse**
> Warehouse create_warehouse(warehouse => $warehouse)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseApi;
my $api_instance = WWW::OpenAPIClient::WarehouseApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse = WWW::OpenAPIClient::Object::Warehouse->new(); # Warehouse | 

eval {
    my $result = $api_instance->create_warehouse(warehouse => $warehouse);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WarehouseApi->create_warehouse: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse** | [**Warehouse**](Warehouse.md)|  | 

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_warehouse**
> delete_warehouse(warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseApi;
my $api_instance = WWW::OpenAPIClient::WarehouseApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse_id = "warehouse_id_example"; # string | 

eval {
    $api_instance->delete_warehouse(warehouse_id => $warehouse_id);
};
if ($@) {
    warn "Exception when calling WarehouseApi->delete_warehouse: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_warehouse**
> Warehouse get_warehouse(warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseApi;
my $api_instance = WWW::OpenAPIClient::WarehouseApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse_id = "warehouse_id_example"; # string | 

eval {
    my $result = $api_instance->get_warehouse(warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WarehouseApi->get_warehouse: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse_id** | **string**|  | 

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_warehouses**
> ARRAY[Warehouse] list_warehouses(page => $page, page_size => $page_size, search => $search, is_active => $is_active)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseApi;
my $api_instance = WWW::OpenAPIClient::WarehouseApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $is_active = null; # boolean | 

eval {
    my $result = $api_instance->list_warehouses(page => $page, page_size => $page_size, search => $search, is_active => $is_active);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WarehouseApi->list_warehouses: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **is_active** | **boolean**|  | [optional] 

### Return type

[**ARRAY[Warehouse]**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_warehouse**
> Warehouse update_warehouse(warehouse_id => $warehouse_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WarehouseApi;
my $api_instance = WWW::OpenAPIClient::WarehouseApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $warehouse_id = "warehouse_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_warehouse(warehouse_id => $warehouse_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WarehouseApi->update_warehouse: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **warehouse_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Warehouse**](Warehouse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

