# WWW::OpenAPIClient::OrderApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::OrderApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_order_tags**](OrderApi.md#add_order_tags) | **POST** /api/v1/orders/{order_id}/tags | 
[**find_order_by_external_ref**](OrderApi.md#find_order_by_external_ref) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} | 
[**get_order**](OrderApi.md#get_order) | **GET** /api/v1/order/{order_number} | 
[**get_orders**](OrderApi.md#get_orders) | **GET** /api/v1/orders | 
[**patch_order**](OrderApi.md#patch_order) | **PATCH** /api/v1/orders/{order_id} | 
[**replace_order_tags**](OrderApi.md#replace_order_tags) | **PUT** /api/v1/orders/{order_id}/tags | 
[**update_order_state**](OrderApi.md#update_order_state) | **PUT** /api/v1/orders/{order_id}/state | 


# **add_order_tags**
> Order add_order_tags(order_id => $order_id, order_tags_request => $order_tags_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderApi;
my $api_instance = WWW::OpenAPIClient::OrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_id = "order_id_example"; # string | 
my $order_tags_request = WWW::OpenAPIClient::Object::OrderTagsRequest->new(); # OrderTagsRequest | 

eval {
    my $result = $api_instance->add_order_tags(order_id => $order_id, order_tags_request => $order_tags_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderApi->add_order_tags: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**|  | 
 **order_tags_request** | [**OrderTagsRequest**](OrderTagsRequest.md)|  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **find_order_by_external_ref**
> Order find_order_by_external_ref(ext_ref => $ext_ref)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderApi;
my $api_instance = WWW::OpenAPIClient::OrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ext_ref = "ext_ref_example"; # string | 

eval {
    my $result = $api_instance->find_order_by_external_ref(ext_ref => $ext_ref);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderApi->find_order_by_external_ref: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ext_ref** | **string**|  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_order**
> Order get_order(order_number => $order_number)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderApi;
my $api_instance = WWW::OpenAPIClient::OrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->get_order(order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderApi->get_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_orders**
> ARRAY[Order] get_orders(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderApi;
my $api_instance = WWW::OpenAPIClient::OrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_orders(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderApi->get_orders: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **include_deleted** | **boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**ARRAY[Order]**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_order**
> Order patch_order(order_id => $order_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderApi;
my $api_instance = WWW::OpenAPIClient::OrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_id = "order_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->patch_order(order_id => $order_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderApi->patch_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replace_order_tags**
> Order replace_order_tags(order_id => $order_id, order_tags_request => $order_tags_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderApi;
my $api_instance = WWW::OpenAPIClient::OrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_id = "order_id_example"; # string | 
my $order_tags_request = WWW::OpenAPIClient::Object::OrderTagsRequest->new(); # OrderTagsRequest | 

eval {
    my $result = $api_instance->replace_order_tags(order_id => $order_id, order_tags_request => $order_tags_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderApi->replace_order_tags: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**|  | 
 **order_tags_request** | [**OrderTagsRequest**](OrderTagsRequest.md)|  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_order_state**
> Order update_order_state(order_id => $order_id, order_state_update => $order_state_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderApi;
my $api_instance = WWW::OpenAPIClient::OrderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_id = "order_id_example"; # string | 
my $order_state_update = WWW::OpenAPIClient::Object::OrderStateUpdate->new(); # OrderStateUpdate | 

eval {
    my $result = $api_instance->update_order_state(order_id => $order_id, order_state_update => $order_state_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderApi->update_order_state: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_id** | **string**|  | 
 **order_state_update** | [**OrderStateUpdate**](OrderStateUpdate.md)|  | 

### Return type

[**Order**](Order.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

