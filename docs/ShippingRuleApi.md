# WWW::OpenAPIClient::ShippingRuleApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ShippingRuleApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_shipping_rule**](ShippingRuleApi.md#create_shipping_rule) | **POST** /api/v1/shipping-rules | 
[**delete_shipping_rule**](ShippingRuleApi.md#delete_shipping_rule) | **DELETE** /api/v1/shipping-rules/{rule_id} | 
[**get_shipping_rule**](ShippingRuleApi.md#get_shipping_rule) | **GET** /api/v1/shipping-rules/{rule_id} | 
[**list_shipping_rules**](ShippingRuleApi.md#list_shipping_rules) | **GET** /api/v1/shipping-rules/ | 
[**update_shipping_rule**](ShippingRuleApi.md#update_shipping_rule) | **PUT** /api/v1/shipping-rules/{rule_id} | 


# **create_shipping_rule**
> ShippingRule create_shipping_rule(shipping_rule_create => $shipping_rule_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingRuleApi;
my $api_instance = WWW::OpenAPIClient::ShippingRuleApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipping_rule_create = WWW::OpenAPIClient::Object::ShippingRuleCreate->new(); # ShippingRuleCreate | 

eval {
    my $result = $api_instance->create_shipping_rule(shipping_rule_create => $shipping_rule_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingRuleApi->create_shipping_rule: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipping_rule_create** | [**ShippingRuleCreate**](ShippingRuleCreate.md)|  | 

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_shipping_rule**
> delete_shipping_rule(rule_id => $rule_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingRuleApi;
my $api_instance = WWW::OpenAPIClient::ShippingRuleApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rule_id = "rule_id_example"; # string | 

eval {
    $api_instance->delete_shipping_rule(rule_id => $rule_id);
};
if ($@) {
    warn "Exception when calling ShippingRuleApi->delete_shipping_rule: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rule_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_shipping_rule**
> ShippingRule get_shipping_rule(rule_id => $rule_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingRuleApi;
my $api_instance = WWW::OpenAPIClient::ShippingRuleApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rule_id = "rule_id_example"; # string | 

eval {
    my $result = $api_instance->get_shipping_rule(rule_id => $rule_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingRuleApi->get_shipping_rule: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rule_id** | **string**|  | 

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_shipping_rules**
> ARRAY[ShippingRule] list_shipping_rules(page => $page, page_size => $page_size, country => $country)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingRuleApi;
my $api_instance = WWW::OpenAPIClient::ShippingRuleApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $country = "country_example"; # string | 

eval {
    my $result = $api_instance->list_shipping_rules(page => $page, page_size => $page_size, country => $country);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingRuleApi->list_shipping_rules: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **country** | **string**|  | [optional] 

### Return type

[**ARRAY[ShippingRule]**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_shipping_rule**
> ShippingRule update_shipping_rule(rule_id => $rule_id, shipping_rule_update => $shipping_rule_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingRuleApi;
my $api_instance = WWW::OpenAPIClient::ShippingRuleApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rule_id = "rule_id_example"; # string | 
my $shipping_rule_update = WWW::OpenAPIClient::Object::ShippingRuleUpdate->new(); # ShippingRuleUpdate | 

eval {
    my $result = $api_instance->update_shipping_rule(rule_id => $rule_id, shipping_rule_update => $shipping_rule_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingRuleApi->update_shipping_rule: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rule_id** | **string**|  | 
 **shipping_rule_update** | [**ShippingRuleUpdate**](ShippingRuleUpdate.md)|  | 

### Return type

[**ShippingRule**](ShippingRule.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

