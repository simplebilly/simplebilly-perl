# WWW::OpenAPIClient::CouponApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::CouponApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**coupon_restore**](CouponApi.md#coupon_restore) | **POST** /api/v1/coupons/{coupon_id}/restore | 
[**create_coupon**](CouponApi.md#create_coupon) | **POST** /api/v1/coupons | 
[**delete_coupon**](CouponApi.md#delete_coupon) | **DELETE** /api/v1/coupons/{coupon_id} | 
[**get_coupon**](CouponApi.md#get_coupon) | **GET** /api/v1/coupons/{coupon_id} | 
[**list_coupons**](CouponApi.md#list_coupons) | **GET** /api/v1/coupons/ | 
[**update_coupon**](CouponApi.md#update_coupon) | **PUT** /api/v1/coupons/{coupon_id} | 


# **coupon_restore**
> Coupon coupon_restore(coupon_id => $coupon_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CouponApi;
my $api_instance = WWW::OpenAPIClient::CouponApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $coupon_id = "coupon_id_example"; # string | 

eval {
    my $result = $api_instance->coupon_restore(coupon_id => $coupon_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CouponApi->coupon_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **coupon_id** | **string**|  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_coupon**
> Coupon create_coupon(coupon_create => $coupon_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CouponApi;
my $api_instance = WWW::OpenAPIClient::CouponApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $coupon_create = WWW::OpenAPIClient::Object::CouponCreate->new(); # CouponCreate | 

eval {
    my $result = $api_instance->create_coupon(coupon_create => $coupon_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CouponApi->create_coupon: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **coupon_create** | [**CouponCreate**](CouponCreate.md)|  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_coupon**
> delete_coupon(coupon_id => $coupon_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CouponApi;
my $api_instance = WWW::OpenAPIClient::CouponApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $coupon_id = "coupon_id_example"; # string | 

eval {
    $api_instance->delete_coupon(coupon_id => $coupon_id);
};
if ($@) {
    warn "Exception when calling CouponApi->delete_coupon: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **coupon_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_coupon**
> Coupon get_coupon(coupon_id => $coupon_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CouponApi;
my $api_instance = WWW::OpenAPIClient::CouponApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $coupon_id = "coupon_id_example"; # string | 

eval {
    my $result = $api_instance->get_coupon(coupon_id => $coupon_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CouponApi->get_coupon: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **coupon_id** | **string**|  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_coupons**
> ARRAY[Coupon] list_coupons(page => $page, page_size => $page_size, is_active => $is_active, code => $code, discount_type => $discount_type)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CouponApi;
my $api_instance = WWW::OpenAPIClient::CouponApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $is_active = null; # boolean | 
my $code = "code_example"; # string | 
my $discount_type = "discount_type_example"; # string | 

eval {
    my $result = $api_instance->list_coupons(page => $page, page_size => $page_size, is_active => $is_active, code => $code, discount_type => $discount_type);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CouponApi->list_coupons: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **is_active** | **boolean**|  | [optional] 
 **code** | **string**|  | [optional] 
 **discount_type** | **string**|  | [optional] 

### Return type

[**ARRAY[Coupon]**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_coupon**
> Coupon update_coupon(coupon_id => $coupon_id, coupon_update => $coupon_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CouponApi;
my $api_instance = WWW::OpenAPIClient::CouponApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $coupon_id = "coupon_id_example"; # string | 
my $coupon_update = WWW::OpenAPIClient::Object::CouponUpdate->new(); # CouponUpdate | 

eval {
    my $result = $api_instance->update_coupon(coupon_id => $coupon_id, coupon_update => $coupon_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CouponApi->update_coupon: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **coupon_id** | **string**|  | 
 **coupon_update** | [**CouponUpdate**](CouponUpdate.md)|  | 

### Return type

[**Coupon**](Coupon.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

