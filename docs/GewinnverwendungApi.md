# WWW::OpenAPIClient::GewinnverwendungApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GewinnverwendungApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**gewinnverwendung_api**](GewinnverwendungApi.md#gewinnverwendung_api) | **GET** /api/v1/bookkeeping/gewinnverwendung | 
[**gewinnverwendung_export_api**](GewinnverwendungApi.md#gewinnverwendung_export_api) | **GET** /api/v1/bookkeeping/gewinnverwendung/export | 


# **gewinnverwendung_api**
> GewinnverwendungsReport gewinnverwendung_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GewinnverwendungApi;
my $api_instance = WWW::OpenAPIClient::GewinnverwendungApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->gewinnverwendung_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GewinnverwendungApi->gewinnverwendung_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**GewinnverwendungsReport**](GewinnverwendungsReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gewinnverwendung_export_api**
> GewinnverwendungsExportResponse gewinnverwendung_export_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GewinnverwendungApi;
my $api_instance = WWW::OpenAPIClient::GewinnverwendungApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->gewinnverwendung_export_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GewinnverwendungApi->gewinnverwendung_export_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**GewinnverwendungsExportResponse**](GewinnverwendungsExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

