# WWW::OpenAPIClient::AnlageGApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AnlageGApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**anlage_g_api**](AnlageGApi.md#anlage_g_api) | **GET** /api/v1/bookkeeping/anlage-g | 


# **anlage_g_api**
> AnlageGErgebnis anlage_g_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AnlageGApi;
my $api_instance = WWW::OpenAPIClient::AnlageGApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->anlage_g_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AnlageGApi->anlage_g_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**AnlageGErgebnis**](AnlageGErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

