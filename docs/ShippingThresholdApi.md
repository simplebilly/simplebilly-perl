# WWW::OpenAPIClient::ShippingThresholdApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ShippingThresholdApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_shipping_threshold**](ShippingThresholdApi.md#create_shipping_threshold) | **POST** /api/v1/shipping-thresholds | 
[**delete_shipping_threshold**](ShippingThresholdApi.md#delete_shipping_threshold) | **DELETE** /api/v1/shipping-thresholds/{threshold_id} | 
[**get_deliverable**](ShippingThresholdApi.md#get_deliverable) | **GET** /api/v1/shipping-thresholds/deliverable | 
[**get_shipping_threshold**](ShippingThresholdApi.md#get_shipping_threshold) | **GET** /api/v1/shipping-thresholds/{threshold_id} | 
[**list_shipping_thresholds**](ShippingThresholdApi.md#list_shipping_thresholds) | **GET** /api/v1/shipping-thresholds/ | 
[**update_shipping_threshold**](ShippingThresholdApi.md#update_shipping_threshold) | **PUT** /api/v1/shipping-thresholds/{threshold_id} | 


# **create_shipping_threshold**
> ShippingThreshold create_shipping_threshold(shipping_threshold_create => $shipping_threshold_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingThresholdApi;
my $api_instance = WWW::OpenAPIClient::ShippingThresholdApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipping_threshold_create = WWW::OpenAPIClient::Object::ShippingThresholdCreate->new(); # ShippingThresholdCreate | 

eval {
    my $result = $api_instance->create_shipping_threshold(shipping_threshold_create => $shipping_threshold_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingThresholdApi->create_shipping_threshold: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipping_threshold_create** | [**ShippingThresholdCreate**](ShippingThresholdCreate.md)|  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_shipping_threshold**
> delete_shipping_threshold(threshold_id => $threshold_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingThresholdApi;
my $api_instance = WWW::OpenAPIClient::ShippingThresholdApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $threshold_id = "threshold_id_example"; # string | 

eval {
    $api_instance->delete_shipping_threshold(threshold_id => $threshold_id);
};
if ($@) {
    warn "Exception when calling ShippingThresholdApi->delete_shipping_threshold: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **threshold_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_deliverable**
> DeliverableResponse get_deliverable(product_id => $product_id, warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingThresholdApi;
my $api_instance = WWW::OpenAPIClient::ShippingThresholdApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 
my $warehouse_id = "warehouse_id_example"; # string | 

eval {
    my $result = $api_instance->get_deliverable(product_id => $product_id, warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingThresholdApi->get_deliverable: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 
 **warehouse_id** | **string**|  | [optional] 

### Return type

[**DeliverableResponse**](DeliverableResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_shipping_threshold**
> ShippingThreshold get_shipping_threshold(threshold_id => $threshold_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingThresholdApi;
my $api_instance = WWW::OpenAPIClient::ShippingThresholdApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $threshold_id = "threshold_id_example"; # string | 

eval {
    my $result = $api_instance->get_shipping_threshold(threshold_id => $threshold_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingThresholdApi->get_shipping_threshold: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **threshold_id** | **string**|  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_shipping_thresholds**
> ARRAY[ShippingThreshold] list_shipping_thresholds(page => $page, page_size => $page_size, product_id => $product_id, warehouse_id => $warehouse_id, is_active => $is_active)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingThresholdApi;
my $api_instance = WWW::OpenAPIClient::ShippingThresholdApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $product_id = "product_id_example"; # string | 
my $warehouse_id = "warehouse_id_example"; # string | 
my $is_active = null; # boolean | 

eval {
    my $result = $api_instance->list_shipping_thresholds(page => $page, page_size => $page_size, product_id => $product_id, warehouse_id => $warehouse_id, is_active => $is_active);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingThresholdApi->list_shipping_thresholds: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **product_id** | **string**|  | [optional] 
 **warehouse_id** | **string**|  | [optional] 
 **is_active** | **boolean**|  | [optional] 

### Return type

[**ARRAY[ShippingThreshold]**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_shipping_threshold**
> ShippingThreshold update_shipping_threshold(threshold_id => $threshold_id, shipping_threshold_update => $shipping_threshold_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingThresholdApi;
my $api_instance = WWW::OpenAPIClient::ShippingThresholdApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $threshold_id = "threshold_id_example"; # string | 
my $shipping_threshold_update = WWW::OpenAPIClient::Object::ShippingThresholdUpdate->new(); # ShippingThresholdUpdate | 

eval {
    my $result = $api_instance->update_shipping_threshold(threshold_id => $threshold_id, shipping_threshold_update => $shipping_threshold_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingThresholdApi->update_shipping_threshold: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **threshold_id** | **string**|  | 
 **shipping_threshold_update** | [**ShippingThresholdUpdate**](ShippingThresholdUpdate.md)|  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

