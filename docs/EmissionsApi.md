# WWW::OpenAPIClient::EmissionsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::EmissionsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_emission_entry_api**](EmissionsApi.md#create_emission_entry_api) | **POST** /api/v1/bookkeeping/emissions/entries | 
[**create_emission_target_api**](EmissionsApi.md#create_emission_target_api) | **POST** /api/v1/bookkeeping/emissions/targets | 
[**delete_emission_entry_api**](EmissionsApi.md#delete_emission_entry_api) | **DELETE** /api/v1/bookkeeping/emissions/entries/{id} | 
[**delete_emission_target_api**](EmissionsApi.md#delete_emission_target_api) | **DELETE** /api/v1/bookkeeping/emissions/targets/{id} | 
[**emissions_entries_api**](EmissionsApi.md#emissions_entries_api) | **GET** /api/v1/bookkeeping/emissions/entries | 
[**emissions_export_api**](EmissionsApi.md#emissions_export_api) | **GET** /api/v1/bookkeeping/emissions/export | 
[**emissions_factors_api**](EmissionsApi.md#emissions_factors_api) | **GET** /api/v1/bookkeeping/emissions/factors | 
[**emissions_report_api**](EmissionsApi.md#emissions_report_api) | **GET** /api/v1/bookkeeping/emissions/report | 
[**emissions_targets_api**](EmissionsApi.md#emissions_targets_api) | **GET** /api/v1/bookkeeping/emissions/targets | 


# **create_emission_entry_api**
> EmissionEntry create_emission_entry_api(create_emission_entry => $create_emission_entry)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $create_emission_entry = WWW::OpenAPIClient::Object::CreateEmissionEntry->new(); # CreateEmissionEntry | 

eval {
    my $result = $api_instance->create_emission_entry_api(create_emission_entry => $create_emission_entry);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmissionsApi->create_emission_entry_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_emission_entry** | [**CreateEmissionEntry**](CreateEmissionEntry.md)|  | 

### Return type

[**EmissionEntry**](EmissionEntry.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_emission_target_api**
> EmissionTarget create_emission_target_api(create_emission_target => $create_emission_target)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $create_emission_target = WWW::OpenAPIClient::Object::CreateEmissionTarget->new(); # CreateEmissionTarget | 

eval {
    my $result = $api_instance->create_emission_target_api(create_emission_target => $create_emission_target);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmissionsApi->create_emission_target_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_emission_target** | [**CreateEmissionTarget**](CreateEmissionTarget.md)|  | 

### Return type

[**EmissionTarget**](EmissionTarget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_emission_entry_api**
> delete_emission_entry_api(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_emission_entry_api(id => $id);
};
if ($@) {
    warn "Exception when calling EmissionsApi->delete_emission_entry_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_emission_target_api**
> delete_emission_target_api(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_emission_target_api(id => $id);
};
if ($@) {
    warn "Exception when calling EmissionsApi->delete_emission_target_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissions_entries_api**
> ARRAY[EmissionEntry] emissions_entries_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->emissions_entries_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmissionsApi->emissions_entries_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**ARRAY[EmissionEntry]**](EmissionEntry.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissions_export_api**
> EmissionsExportResponse emissions_export_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->emissions_export_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmissionsApi->emissions_export_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**EmissionsExportResponse**](EmissionsExportResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissions_factors_api**
> ARRAY[EmissionFactorResponse] emissions_factors_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->emissions_factors_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmissionsApi->emissions_factors_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[EmissionFactorResponse]**](EmissionFactorResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissions_report_api**
> EmissionsReport emissions_report_api(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->emissions_report_api(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmissionsApi->emissions_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**EmissionsReport**](EmissionsReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emissions_targets_api**
> ARRAY[EmissionTarget] emissions_targets_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmissionsApi;
my $api_instance = WWW::OpenAPIClient::EmissionsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->emissions_targets_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmissionsApi->emissions_targets_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[EmissionTarget]**](EmissionTarget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

