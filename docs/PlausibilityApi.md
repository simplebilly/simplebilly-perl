# WWW::OpenAPIClient::PlausibilityApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PlausibilityApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**plausibility_check_api**](PlausibilityApi.md#plausibility_check_api) | **GET** /api/v1/bookkeeping/plausibility | 


# **plausibility_check_api**
> PlausibilityReport plausibility_check_api(date_from => $date_from, date_to => $date_to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PlausibilityApi;
my $api_instance = WWW::OpenAPIClient::PlausibilityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 

eval {
    my $result = $api_instance->plausibility_check_api(date_from => $date_from, date_to => $date_to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PlausibilityApi->plausibility_check_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 

### Return type

[**PlausibilityReport**](PlausibilityReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

