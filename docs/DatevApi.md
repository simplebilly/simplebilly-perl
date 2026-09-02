# WWW::OpenAPIClient::DatevApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DatevApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**datev_export_api**](DatevApi.md#datev_export_api) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV
[**datev_preview_api**](DatevApi.md#datev_preview_api) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review


# **datev_export_api**
> DatevExportResponse datev_export_api(account_schema => $account_schema, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size)

Export bookkeeping data as DATEV CSV

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DatevApi;
my $api_instance = WWW::OpenAPIClient::DatevApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $account_schema = "account_schema_example"; # string | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->datev_export_api(account_schema => $account_schema, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DatevApi->datev_export_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_schema** | **string**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**DatevExportResponse**](DatevExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **datev_preview_api**
> ARRAY[DatevBookingPreview] datev_preview_api(account_schema => $account_schema, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size)

Exported_datev_bookings: returns formed bookings for review

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DatevApi;
my $api_instance = WWW::OpenAPIClient::DatevApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $account_schema = "account_schema_example"; # string | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->datev_preview_api(account_schema => $account_schema, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DatevApi->datev_preview_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_schema** | **string**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**ARRAY[DatevBookingPreview]**](DatevBookingPreview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

