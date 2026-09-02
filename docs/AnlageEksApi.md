# WWW::OpenAPIClient::AnlageEksApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AnlageEksApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**eks_api**](AnlageEksApi.md#eks_api) | **GET** /api/v1/bookkeeping/eks | 


# **eks_api**
> EksErgebnis eks_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AnlageEksApi;
my $api_instance = WWW::OpenAPIClient::AnlageEksApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->eks_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AnlageEksApi->eks_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**EksErgebnis**](EksErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

