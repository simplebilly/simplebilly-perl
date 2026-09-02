# WWW::OpenAPIClient::ShippingApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ShippingApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_credentials_api**](ShippingApi.md#get_credentials_api) | **GET** /api/v1/shipping/credentials | 
[**get_rates_api**](ShippingApi.md#get_rates_api) | **POST** /api/v1/shipping/rates | 
[**list_providers_api**](ShippingApi.md#list_providers_api) | **GET** /api/v1/shipping/providers | 
[**save_credentials_api**](ShippingApi.md#save_credentials_api) | **PUT** /api/v1/shipping/credentials | 


# **get_credentials_api**
> ShippingCredentials get_credentials_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingApi;
my $api_instance = WWW::OpenAPIClient::ShippingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_credentials_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingApi->get_credentials_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_rates_api**
> RateResponse get_rates_api(rate_request => $rate_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingApi;
my $api_instance = WWW::OpenAPIClient::ShippingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rate_request = WWW::OpenAPIClient::Object::RateRequest->new(); # RateRequest | 

eval {
    my $result = $api_instance->get_rates_api(rate_request => $rate_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingApi->get_rates_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rate_request** | [**RateRequest**](RateRequest.md)|  | 

### Return type

[**RateResponse**](RateResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_providers_api**
> ARRAY[ProviderInfo] list_providers_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingApi;
my $api_instance = WWW::OpenAPIClient::ShippingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_providers_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingApi->list_providers_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[ProviderInfo]**](ProviderInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **save_credentials_api**
> ShippingCredentials save_credentials_api(shipping_credentials => $shipping_credentials)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShippingApi;
my $api_instance = WWW::OpenAPIClient::ShippingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipping_credentials = WWW::OpenAPIClient::Object::ShippingCredentials->new(); # ShippingCredentials | 

eval {
    my $result = $api_instance->save_credentials_api(shipping_credentials => $shipping_credentials);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShippingApi->save_credentials_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipping_credentials** | [**ShippingCredentials**](ShippingCredentials.md)|  | 

### Return type

[**ShippingCredentials**](ShippingCredentials.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

