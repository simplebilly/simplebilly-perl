# WWW::OpenAPIClient::AdminApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AdminApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**trigger_mirror**](AdminApi.md#trigger_mirror) | **POST** /api/v1/admin/storage/mirror | 


# **trigger_mirror**
> MirrorTriggerResponse trigger_mirror()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AdminApi;
my $api_instance = WWW::OpenAPIClient::AdminApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->trigger_mirror();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AdminApi->trigger_mirror: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**MirrorTriggerResponse**](MirrorTriggerResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

