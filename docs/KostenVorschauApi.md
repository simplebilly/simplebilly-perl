# WWW::OpenAPIClient::KostenVorschauApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::KostenVorschauApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**kosten_vorschau_api**](KostenVorschauApi.md#kosten_vorschau_api) | **GET** /api/v1/bookkeeping/kosten-vorschau | 


# **kosten_vorschau_api**
> KostenVorschau kosten_vorschau_api(year => $year, month => $month)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KostenVorschauApi;
my $api_instance = WWW::OpenAPIClient::KostenVorschauApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 

eval {
    my $result = $api_instance->kosten_vorschau_api(year => $year, month => $month);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KostenVorschauApi->kosten_vorschau_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 
 **month** | **int**|  | 

### Return type

[**KostenVorschau**](KostenVorschau.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

