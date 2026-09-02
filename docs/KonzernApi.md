# WWW::OpenAPIClient::KonzernApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::KonzernApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**konzern_export_api**](KonzernApi.md#konzern_export_api) | **GET** /api/v1/bookkeeping/konzern/status/export | 
[**konzern_status_api**](KonzernApi.md#konzern_status_api) | **GET** /api/v1/bookkeeping/konzern/status | 


# **konzern_export_api**
> KonzernExportResponse konzern_export_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KonzernApi;
my $api_instance = WWW::OpenAPIClient::KonzernApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->konzern_export_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KonzernApi->konzern_export_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**KonzernExportResponse**](KonzernExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **konzern_status_api**
> KonzernStatus konzern_status_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KonzernApi;
my $api_instance = WWW::OpenAPIClient::KonzernApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->konzern_status_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KonzernApi->konzern_status_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**KonzernStatus**](KonzernStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

