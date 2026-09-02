# WWW::OpenAPIClient::PriceTierApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PriceTierApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_price_tier**](PriceTierApi.md#create_price_tier) | **POST** /api/v1/price-tiers | 
[**delete_price_tier**](PriceTierApi.md#delete_price_tier) | **DELETE** /api/v1/price-tiers/{price_tier_id} | 
[**get_price_tier**](PriceTierApi.md#get_price_tier) | **GET** /api/v1/price-tiers/{price_tier_id} | 
[**get_resolved_price**](PriceTierApi.md#get_resolved_price) | **GET** /api/v1/price-tiers/resolved | 
[**list_price_tiers**](PriceTierApi.md#list_price_tiers) | **GET** /api/v1/price-tiers/ | 
[**update_price_tier**](PriceTierApi.md#update_price_tier) | **PUT** /api/v1/price-tiers/{price_tier_id} | 


# **create_price_tier**
> PriceTier create_price_tier(price_tier_create => $price_tier_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PriceTierApi;
my $api_instance = WWW::OpenAPIClient::PriceTierApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $price_tier_create = WWW::OpenAPIClient::Object::PriceTierCreate->new(); # PriceTierCreate | 

eval {
    my $result = $api_instance->create_price_tier(price_tier_create => $price_tier_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PriceTierApi->create_price_tier: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **price_tier_create** | [**PriceTierCreate**](PriceTierCreate.md)|  | 

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_price_tier**
> delete_price_tier(price_tier_id => $price_tier_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PriceTierApi;
my $api_instance = WWW::OpenAPIClient::PriceTierApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $price_tier_id = "price_tier_id_example"; # string | 

eval {
    $api_instance->delete_price_tier(price_tier_id => $price_tier_id);
};
if ($@) {
    warn "Exception when calling PriceTierApi->delete_price_tier: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **price_tier_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_price_tier**
> PriceTier get_price_tier(price_tier_id => $price_tier_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PriceTierApi;
my $api_instance = WWW::OpenAPIClient::PriceTierApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $price_tier_id = "price_tier_id_example"; # string | 

eval {
    my $result = $api_instance->get_price_tier(price_tier_id => $price_tier_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PriceTierApi->get_price_tier: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **price_tier_id** | **string**|  | 

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_resolved_price**
> ResolvedPriceResponse get_resolved_price(product_id => $product_id, quantity => $quantity, contact_id => $contact_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PriceTierApi;
my $api_instance = WWW::OpenAPIClient::PriceTierApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 
my $quantity = 789; # int | 
my $contact_id = "contact_id_example"; # string | Contact used to match customer-group-scoped tiers.

eval {
    my $result = $api_instance->get_resolved_price(product_id => $product_id, quantity => $quantity, contact_id => $contact_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PriceTierApi->get_resolved_price: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 
 **quantity** | **int**|  | [optional] 
 **contact_id** | **string**| Contact used to match customer-group-scoped tiers. | [optional] 

### Return type

[**ResolvedPriceResponse**](ResolvedPriceResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_price_tiers**
> ARRAY[PriceTier] list_price_tiers(page => $page, page_size => $page_size, product_id => $product_id, customer_group_id => $customer_group_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PriceTierApi;
my $api_instance = WWW::OpenAPIClient::PriceTierApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $product_id = "product_id_example"; # string | 
my $customer_group_id = "customer_group_id_example"; # string | 

eval {
    my $result = $api_instance->list_price_tiers(page => $page, page_size => $page_size, product_id => $product_id, customer_group_id => $customer_group_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PriceTierApi->list_price_tiers: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **product_id** | **string**|  | [optional] 
 **customer_group_id** | **string**|  | [optional] 

### Return type

[**ARRAY[PriceTier]**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_price_tier**
> PriceTier update_price_tier(price_tier_id => $price_tier_id, price_tier_update => $price_tier_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PriceTierApi;
my $api_instance = WWW::OpenAPIClient::PriceTierApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $price_tier_id = "price_tier_id_example"; # string | 
my $price_tier_update = WWW::OpenAPIClient::Object::PriceTierUpdate->new(); # PriceTierUpdate | 

eval {
    my $result = $api_instance->update_price_tier(price_tier_id => $price_tier_id, price_tier_update => $price_tier_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PriceTierApi->update_price_tier: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **price_tier_id** | **string**|  | 
 **price_tier_update** | [**PriceTierUpdate**](PriceTierUpdate.md)|  | 

### Return type

[**PriceTier**](PriceTier.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

