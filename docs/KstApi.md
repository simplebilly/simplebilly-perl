# WWW::OpenAPIClient::KstApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::KstApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**kst_api**](KstApi.md#kst_api) | **GET** /api/v1/bookkeeping/kst | 


# **kst_api**
> KstErgebnis kst_api(year => $year, gewinn => $gewinn)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KstApi;
my $api_instance = WWW::OpenAPIClient::KstApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $gewinn = "gewinn_example"; # string | 

eval {
    my $result = $api_instance->kst_api(year => $year, gewinn => $gewinn);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KstApi->kst_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 
 **gewinn** | **string**|  | [optional] 

### Return type

[**KstErgebnis**](KstErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

