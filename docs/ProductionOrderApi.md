# WWW::OpenAPIClient::ProductionOrderApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ProductionOrderApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_production_order**](ProductionOrderApi.md#create_production_order) | **POST** /api/v1/production-orders | 
[**delete_production_order**](ProductionOrderApi.md#delete_production_order) | **DELETE** /api/v1/production-orders/{production_order_id} | 
[**get_production_order**](ProductionOrderApi.md#get_production_order) | **GET** /api/v1/production-orders/{production_order_id} | 
[**list_production_orders**](ProductionOrderApi.md#list_production_orders) | **GET** /api/v1/production-orders/ | 
[**production_order_costing**](ProductionOrderApi.md#production_order_costing) | **GET** /api/v1/production-orders/{production_order_id}/costing | Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product&#39;s sale price.
[**update_production_order**](ProductionOrderApi.md#update_production_order) | **PUT** /api/v1/production-orders/{production_order_id} | 
[**update_production_order_status**](ProductionOrderApi.md#update_production_order_status) | **PUT** /api/v1/production-orders/{production_order_id}/status | 


# **create_production_order**
> ProductionOrder create_production_order(production_order => $production_order)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductionOrderApi;
my $api_instance = WWW::OpenAPIClient::ProductionOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $production_order = WWW::OpenAPIClient::Object::ProductionOrder->new(); # ProductionOrder | 

eval {
    my $result = $api_instance->create_production_order(production_order => $production_order);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductionOrderApi->create_production_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **production_order** | [**ProductionOrder**](ProductionOrder.md)|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_production_order**
> delete_production_order(production_order_id => $production_order_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductionOrderApi;
my $api_instance = WWW::OpenAPIClient::ProductionOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $production_order_id = "production_order_id_example"; # string | 

eval {
    $api_instance->delete_production_order(production_order_id => $production_order_id);
};
if ($@) {
    warn "Exception when calling ProductionOrderApi->delete_production_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **production_order_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_production_order**
> ProductionOrder get_production_order(production_order_id => $production_order_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductionOrderApi;
my $api_instance = WWW::OpenAPIClient::ProductionOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $production_order_id = "production_order_id_example"; # string | 

eval {
    my $result = $api_instance->get_production_order(production_order_id => $production_order_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductionOrderApi->get_production_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **production_order_id** | **string**|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_production_orders**
> ARRAY[ProductionOrder] list_production_orders(page => $page, page_size => $page_size, search => $search, status => $status)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductionOrderApi;
my $api_instance = WWW::OpenAPIClient::ProductionOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $status = "status_example"; # string | Filter by status.

eval {
    my $result = $api_instance->list_production_orders(page => $page, page_size => $page_size, search => $search, status => $status);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductionOrderApi->list_production_orders: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **status** | **string**| Filter by status. | [optional] 

### Return type

[**ARRAY[ProductionOrder]**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **production_order_costing**
> ProductionOrderCosting production_order_costing(production_order_id => $production_order_id)

Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductionOrderApi;
my $api_instance = WWW::OpenAPIClient::ProductionOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $production_order_id = "production_order_id_example"; # string | 

eval {
    my $result = $api_instance->production_order_costing(production_order_id => $production_order_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductionOrderApi->production_order_costing: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **production_order_id** | **string**|  | 

### Return type

[**ProductionOrderCosting**](ProductionOrderCosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_production_order**
> ProductionOrder update_production_order(production_order_id => $production_order_id, production_order => $production_order)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductionOrderApi;
my $api_instance = WWW::OpenAPIClient::ProductionOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $production_order_id = "production_order_id_example"; # string | 
my $production_order = WWW::OpenAPIClient::Object::ProductionOrder->new(); # ProductionOrder | 

eval {
    my $result = $api_instance->update_production_order(production_order_id => $production_order_id, production_order => $production_order);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductionOrderApi->update_production_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **production_order_id** | **string**|  | 
 **production_order** | [**ProductionOrder**](ProductionOrder.md)|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_production_order_status**
> ProductionOrder update_production_order_status(production_order_id => $production_order_id, production_order_status_update => $production_order_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductionOrderApi;
my $api_instance = WWW::OpenAPIClient::ProductionOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $production_order_id = "production_order_id_example"; # string | 
my $production_order_status_update = WWW::OpenAPIClient::Object::ProductionOrderStatusUpdate->new(); # ProductionOrderStatusUpdate | 

eval {
    my $result = $api_instance->update_production_order_status(production_order_id => $production_order_id, production_order_status_update => $production_order_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductionOrderApi->update_production_order_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **production_order_id** | **string**|  | 
 **production_order_status_update** | [**ProductionOrderStatusUpdate**](ProductionOrderStatusUpdate.md)|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

