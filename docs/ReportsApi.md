# WWW::OpenAPIClient::ReportsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ReportsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bilanz_report_api**](ReportsApi.md#bilanz_report_api) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet)
[**guv_report_api**](ReportsApi.md#guv_report_api) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement)
[**kontenansicht_report_api**](ReportsApi.md#kontenansicht_report_api) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview)
[**umsatzsteuer_report_api**](ReportsApi.md#umsatzsteuer_report_api) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report)


# **bilanz_report_api**
> BilanzReport bilanz_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size)

Bilanz (Balance Sheet)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReportsApi;
my $api_instance = WWW::OpenAPIClient::ReportsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->bilanz_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReportsApi->bilanz_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **month** | **int**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**BilanzReport**](BilanzReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **guv_report_api**
> GuVReport guv_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size)

Gewinn- und Verlustrechnung (P&L statement)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReportsApi;
my $api_instance = WWW::OpenAPIClient::ReportsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->guv_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReportsApi->guv_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **month** | **int**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**GuVReport**](GuVReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **kontenansicht_report_api**
> KontoReport kontenansicht_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size)

Kontenansicht (Account Overview)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReportsApi;
my $api_instance = WWW::OpenAPIClient::ReportsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->kontenansicht_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReportsApi->kontenansicht_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **month** | **int**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**KontoReport**](KontoReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **umsatzsteuer_report_api**
> UmsatzsteuerReport umsatzsteuer_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size)

Umsatzsteuer-Voranmeldung (VAT report)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReportsApi;
my $api_instance = WWW::OpenAPIClient::ReportsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 
my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->umsatzsteuer_report_api(year => $year, month => $month, date_from => $date_from, date_to => $date_to, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReportsApi->umsatzsteuer_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **month** | **int**|  | [optional] 
 **date_from** | **string**|  | [optional] 
 **date_to** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**UmsatzsteuerReport**](UmsatzsteuerReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

