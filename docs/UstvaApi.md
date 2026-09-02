# WWW::OpenAPIClient::UstvaApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::UstvaApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**jahresust_api**](UstvaApi.md#jahresust_api) | **GET** /api/v1/bookkeeping/jahresust | 
[**ustva_api**](UstvaApi.md#ustva_api) | **GET** /api/v1/bookkeeping/ustva | 


# **jahresust_api**
> JahresUstErgebnis jahresust_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UstvaApi;
my $api_instance = WWW::OpenAPIClient::UstvaApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->jahresust_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UstvaApi->jahresust_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**JahresUstErgebnis**](JahresUstErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ustva_api**
> UstvaErgebnis ustva_api(zeitraum => $zeitraum)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UstvaApi;
my $api_instance = WWW::OpenAPIClient::UstvaApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $zeitraum = "zeitraum_example"; # string | 

eval {
    my $result = $api_instance->ustva_api(zeitraum => $zeitraum);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UstvaApi->ustva_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **zeitraum** | **string**|  | 

### Return type

[**UstvaErgebnis**](UstvaErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

