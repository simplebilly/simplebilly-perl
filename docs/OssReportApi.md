# WWW::OpenAPIClient::OssReportApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::OssReportApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**oss_report_api**](OssReportApi.md#oss_report_api) | **GET** /api/v1/bookkeeping/oss | 


# **oss_report_api**
> OssReport oss_report_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OssReportApi;
my $api_instance = WWW::OpenAPIClient::OssReportApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->oss_report_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OssReportApi->oss_report_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**OssReport**](OssReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

