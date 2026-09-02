# WWW::OpenAPIClient::InstituteApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::InstituteApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**institute_status_api**](InstituteApi.md#institute_status_api) | **GET** /api/v1/bookkeeping/institute/status | 


# **institute_status_api**
> InstituteStatus institute_status_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InstituteApi;
my $api_instance = WWW::OpenAPIClient::InstituteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->institute_status_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InstituteApi->institute_status_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InstituteStatus**](InstituteStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

