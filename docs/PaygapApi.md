# WWW::OpenAPIClient::PaygapApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PaygapApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**paygap_auskunft_api**](PaygapApi.md#paygap_auskunft_api) | **GET** /api/v1/bookkeeping/paygap/auskunft/{employee_id} | 
[**paygap_export_api**](PaygapApi.md#paygap_export_api) | **GET** /api/v1/bookkeeping/paygap/export | 
[**paygap_report_api**](PaygapApi.md#paygap_report_api) | **GET** /api/v1/bookkeeping/paygap/report | 


# **paygap_auskunft_api**
> PayGapInfoResponse paygap_auskunft_api(employee_id => $employee_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaygapApi;
my $api_instance = WWW::OpenAPIClient::PaygapApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $employee_id = "employee_id_example"; # string | 

eval {
    my $result = $api_instance->paygap_auskunft_api(employee_id => $employee_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaygapApi->paygap_auskunft_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employee_id** | **string**|  | 

### Return type

[**PayGapInfoResponse**](PayGapInfoResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paygap_export_api**
> PayGapExportResponse paygap_export_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaygapApi;
my $api_instance = WWW::OpenAPIClient::PaygapApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->paygap_export_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaygapApi->paygap_export_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PayGapExportResponse**](PayGapExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paygap_report_api**
> PayGapReport paygap_report_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaygapApi;
my $api_instance = WWW::OpenAPIClient::PaygapApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->paygap_report_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaygapApi->paygap_report_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PayGapReport**](PayGapReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

