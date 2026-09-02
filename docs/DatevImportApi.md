# WWW::OpenAPIClient::DatevImportApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DatevImportApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**datev_import_api**](DatevImportApi.md#datev_import_api) | **POST** /api/v1/bookkeeping/datev/import | 


# **datev_import_api**
> DatevImportResponse datev_import_api(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DatevImportApi;
my $api_instance = WWW::OpenAPIClient::DatevImportApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->datev_import_api(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DatevImportApi->datev_import_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**DatevImportResponse**](DatevImportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

