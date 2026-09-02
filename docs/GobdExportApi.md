# WWW::OpenAPIClient::GobdExportApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GobdExportApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**buchhalter_csv_api**](GobdExportApi.md#buchhalter_csv_api) | **GET** /api/v1/bookkeeping/buchhalter-csv | 
[**gobd_export_api**](GobdExportApi.md#gobd_export_api) | **GET** /api/v1/bookkeeping/gobd | GoBD/GDPdU export. Default: ZIP archive (&#x60;index.xml&#x60; + CSV tables, IDEA format). &#x60;?format&#x3D;csv&#x60; returns the legacy single-journal CSV as JSON.


# **buchhalter_csv_api**
> GoBDExportResponse buchhalter_csv_api(date_from => $date_from, date_to => $date_to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GobdExportApi;
my $api_instance = WWW::OpenAPIClient::GobdExportApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $date_from = "date_from_example"; # string | 
my $date_to = "date_to_example"; # string | 

eval {
    my $result = $api_instance->buchhalter_csv_api(date_from => $date_from, date_to => $date_to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GobdExportApi->buchhalter_csv_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **date_from** | **string**|  | 
 **date_to** | **string**|  | 

### Return type

[**GoBDExportResponse**](GoBDExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **gobd_export_api**
> gobd_export_api(year => $year, format => $format)

GoBD/GDPdU export. Default: ZIP archive (`index.xml` + CSV tables, IDEA format). `?format=csv` returns the legacy single-journal CSV as JSON.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GobdExportApi;
my $api_instance = WWW::OpenAPIClient::GobdExportApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $format = zip; # string | Export format: `zip` (default, full GDPdU/IDEA export) or `csv` (legacy single-journal CSV as JSON).

eval {
    $api_instance->gobd_export_api(year => $year, format => $format);
};
if ($@) {
    warn "Exception when calling GobdExportApi->gobd_export_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 
 **format** | **string**| Export format: &#x60;zip&#x60; (default, full GDPdU/IDEA export) or &#x60;csv&#x60; (legacy single-journal CSV as JSON). | [optional] 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/zip, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

