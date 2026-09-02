# WWW::OpenAPIClient::StilleApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::StilleApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**stille_export_api**](StilleApi.md#stille_export_api) | **GET** /api/v1/bookkeeping/stille/export | 
[**stille_report_api**](StilleApi.md#stille_report_api) | **GET** /api/v1/bookkeeping/stille/report | 


# **stille_export_api**
> StilleExportResponse stille_export_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StilleApi;
my $api_instance = WWW::OpenAPIClient::StilleApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->stille_export_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StilleApi->stille_export_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**StilleExportResponse**](StilleExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **stille_report_api**
> StilleReport stille_report_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::StilleApi;
my $api_instance = WWW::OpenAPIClient::StilleApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->stille_report_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling StilleApi->stille_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**StilleReport**](StilleReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

