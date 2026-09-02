# WWW::OpenAPIClient::EbilanzApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::EbilanzApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ebilanz_report_api**](EbilanzApi.md#ebilanz_report_api) | **GET** /api/v1/bookkeeping/ebilanz | 
[**ebilanz_xbrl_export_api**](EbilanzApi.md#ebilanz_xbrl_export_api) | **GET** /api/v1/bookkeeping/ebilanz/xbrl | 


# **ebilanz_report_api**
> EBilanzReport ebilanz_report_api(year => $year, date_from => $date_from, date_to => $date_to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EbilanzApi;
my $api_instance = WWW::OpenAPIClient::EbilanzApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 

eval {
    my $result = $api_instance->ebilanz_report_api(year => $year, date_from => $date_from, date_to => $date_to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EbilanzApi->ebilanz_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 

### Return type

[**EBilanzReport**](EBilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ebilanz_xbrl_export_api**
> ebilanz_xbrl_export_api(year => $year, date_from => $date_from, date_to => $date_to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EbilanzApi;
my $api_instance = WWW::OpenAPIClient::EbilanzApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 

eval {
    $api_instance->ebilanz_xbrl_export_api(year => $year, date_from => $date_from, date_to => $date_to);
};
if ($@) {
    warn "Exception when calling EbilanzApi->ebilanz_xbrl_export_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

