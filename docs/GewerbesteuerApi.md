# WWW::OpenAPIClient::GewerbesteuerApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GewerbesteuerApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gewerbesteuer_api**](GewerbesteuerApi.md#gewerbesteuer_api) | **GET** /api/v1/bookkeeping/gewerbesteuer | 


# **gewerbesteuer_api**
> GewerbesteuerErgebnis gewerbesteuer_api(year => $year, hebesatz => $hebesatz, gewerbeertrag => $gewerbeertrag, country => $country, gemeindeschluessel => $gemeindeschluessel)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GewerbesteuerApi;
my $api_instance = WWW::OpenAPIClient::GewerbesteuerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $hebesatz = "hebesatz_example"; # string | 
my $gewerbeertrag = "gewerbeertrag_example"; # string | 
my $country = "country_example"; # string | 
my $gemeindeschluessel = "gemeindeschluessel_example"; # string | 

eval {
    my $result = $api_instance->gewerbesteuer_api(year => $year, hebesatz => $hebesatz, gewerbeertrag => $gewerbeertrag, country => $country, gemeindeschluessel => $gemeindeschluessel);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GewerbesteuerApi->gewerbesteuer_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 
 **hebesatz** | **string**|  | [optional] 
 **gewerbeertrag** | **string**|  | [optional] 
 **country** | **string**|  | [optional] 
 **gemeindeschluessel** | **string**|  | [optional] 

### Return type

[**GewerbesteuerErgebnis**](GewerbesteuerErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

