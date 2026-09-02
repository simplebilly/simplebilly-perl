# WWW::OpenAPIClient::ReturnOrderApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ReturnOrderApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_return_order**](ReturnOrderApi.md#create_return_order) | **POST** /api/v1/returns | 
[**delete_return_order**](ReturnOrderApi.md#delete_return_order) | **DELETE** /api/v1/returns/{return_order_id} | 
[**get_return_order**](ReturnOrderApi.md#get_return_order) | **GET** /api/v1/returns/{return_order_id} | 
[**list_return_orders**](ReturnOrderApi.md#list_return_orders) | **GET** /api/v1/returns/ | 
[**return_logistics_queue**](ReturnOrderApi.md#return_logistics_queue) | **GET** /api/v1/returns/logistics-queue | 
[**return_logistics_summary**](ReturnOrderApi.md#return_logistics_summary) | **GET** /api/v1/returns/logistics-summary | Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
[**update_return_order**](ReturnOrderApi.md#update_return_order) | **PUT** /api/v1/returns/{return_order_id} | 
[**update_return_order_status**](ReturnOrderApi.md#update_return_order_status) | **PUT** /api/v1/returns/{return_order_id}/status | 


# **create_return_order**
> ReturnOrder create_return_order(return_order => $return_order)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $return_order = WWW::OpenAPIClient::Object::ReturnOrder->new(); # ReturnOrder | 

eval {
    my $result = $api_instance->create_return_order(return_order => $return_order);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->create_return_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **return_order** | [**ReturnOrder**](ReturnOrder.md)|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_return_order**
> delete_return_order(return_order_id => $return_order_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $return_order_id = "return_order_id_example"; # string | 

eval {
    $api_instance->delete_return_order(return_order_id => $return_order_id);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->delete_return_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **return_order_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_return_order**
> ReturnOrder get_return_order(return_order_id => $return_order_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $return_order_id = "return_order_id_example"; # string | 

eval {
    my $result = $api_instance->get_return_order(return_order_id => $return_order_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->get_return_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **return_order_id** | **string**|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_return_orders**
> ARRAY[ReturnOrder] list_return_orders(page => $page, page_size => $page_size, status => $status, customer_name => $customer_name, order_number => $order_number)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $customer_name = "customer_name_example"; # string | 
my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->list_return_orders(page => $page, page_size => $page_size, status => $status, customer_name => $customer_name, order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->list_return_orders: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **customer_name** | **string**|  | [optional] 
 **order_number** | **string**|  | [optional] 

### Return type

[**ARRAY[ReturnOrder]**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **return_logistics_queue**
> ARRAY[ReturnLogisticsQueueItem] return_logistics_queue()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->return_logistics_queue();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->return_logistics_queue: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[ReturnLogisticsQueueItem]**](ReturnLogisticsQueueItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **return_logistics_summary**
> ReturnLogisticsSummary return_logistics_summary()

Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->return_logistics_summary();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->return_logistics_summary: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ReturnLogisticsSummary**](ReturnLogisticsSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_return_order**
> ReturnOrder update_return_order(return_order_id => $return_order_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $return_order_id = "return_order_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_return_order(return_order_id => $return_order_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->update_return_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **return_order_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_return_order_status**
> ReturnOrder update_return_order_status(return_order_id => $return_order_id, return_order_status_update => $return_order_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReturnOrderApi;
my $api_instance = WWW::OpenAPIClient::ReturnOrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $return_order_id = "return_order_id_example"; # string | 
my $return_order_status_update = WWW::OpenAPIClient::Object::ReturnOrderStatusUpdate->new(); # ReturnOrderStatusUpdate | 

eval {
    my $result = $api_instance->update_return_order_status(return_order_id => $return_order_id, return_order_status_update => $return_order_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReturnOrderApi->update_return_order_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **return_order_id** | **string**|  | 
 **return_order_status_update** | [**ReturnOrderStatusUpdate**](ReturnOrderStatusUpdate.md)|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

