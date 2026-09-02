# WWW::OpenAPIClient::GezApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GezApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gez_api**](GezApi.md#gez_api) | **GET** /api/v1/bookkeeping/gez | 


# **gez_api**
> GezReport gez_api(jahr => $jahr, betriebsstaetten => $betriebsstaetten, kfz => $kfz, hotelzimmer => $hotelzimmer, beschaefigte => $beschaefigte)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GezApi;
my $api_instance = WWW::OpenAPIClient::GezApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $jahr = 56; # int | 
my $betriebsstaetten = "betriebsstaetten_example"; # string | Liste der Betriebsstätten als JSON, z.B. `[{\"name\":\"Filiale 1\",\"beschaefigte\":12}]`.
my $kfz = 789; # int | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind).
my $hotelzimmer = 789; # int | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen.
my $beschaefigte = 789; # int | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen).

eval {
    my $result = $api_instance->gez_api(jahr => $jahr, betriebsstaetten => $betriebsstaetten, kfz => $kfz, hotelzimmer => $hotelzimmer, beschaefigte => $beschaefigte);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GezApi->gez_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **jahr** | **int**|  | [optional] 
 **betriebsstaetten** | **string**| Liste der Betriebsstätten als JSON, z.B. &#x60;[{\&quot;name\&quot;:\&quot;Filiale 1\&quot;,\&quot;beschaefigte\&quot;:12}]&#x60;. | [optional] 
 **kfz** | **int**| Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional] 
 **hotelzimmer** | **int**| Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional] 
 **beschaefigte** | **int**| Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional] 

### Return type

[**GezReport**](GezReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

