# WWW::OpenAPIClient::SuitabilityApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::SuitabilityApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**shipping_suitability_api**](SuitabilityApi.md#shipping_suitability_api) | **POST** /api/v1/shipping/suitability | 


# **shipping_suitability_api**
> SuitabilityResult shipping_suitability_api(suitability_request => $suitability_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SuitabilityApi;
my $api_instance = WWW::OpenAPIClient::SuitabilityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $suitability_request = WWW::OpenAPIClient::Object::SuitabilityRequest->new(); # SuitabilityRequest | 

eval {
    my $result = $api_instance->shipping_suitability_api(suitability_request => $suitability_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SuitabilityApi->shipping_suitability_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **suitability_request** | [**SuitabilityRequest**](SuitabilityRequest.md)|  | 

### Return type

[**SuitabilityResult**](SuitabilityResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

