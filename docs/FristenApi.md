# WWW::OpenAPIClient::FristenApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::FristenApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fristen_api**](FristenApi.md#fristen_api) | **GET** /api/v1/bookkeeping/fristen | 


# **fristen_api**
> FristenErgebnis fristen_api(bundesland => $bundesland, voranmeldungsrhythmus => $voranmeldungsrhythmus, dauerfristverlaengerung => $dauerfristverlaengerung, est_aktiv => $est_aktiv, gewst_aktiv => $gewst_aktiv, monate => $monate)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::FristenApi;
my $api_instance = WWW::OpenAPIClient::FristenApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $bundesland = "bundesland_example"; # string | 
my $voranmeldungsrhythmus = "voranmeldungsrhythmus_example"; # string | 
my $dauerfristverlaengerung = null; # boolean | 
my $est_aktiv = null; # boolean | 
my $gewst_aktiv = null; # boolean | 
my $monate = 56; # int | 

eval {
    my $result = $api_instance->fristen_api(bundesland => $bundesland, voranmeldungsrhythmus => $voranmeldungsrhythmus, dauerfristverlaengerung => $dauerfristverlaengerung, est_aktiv => $est_aktiv, gewst_aktiv => $gewst_aktiv, monate => $monate);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling FristenApi->fristen_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bundesland** | **string**|  | [optional] 
 **voranmeldungsrhythmus** | **string**|  | [optional] 
 **dauerfristverlaengerung** | **boolean**|  | [optional] 
 **est_aktiv** | **boolean**|  | [optional] 
 **gewst_aktiv** | **boolean**|  | [optional] 
 **monate** | **int**|  | [optional] 

### Return type

[**FristenErgebnis**](FristenErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

