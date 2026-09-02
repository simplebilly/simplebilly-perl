# WWW::OpenAPIClient::ImportRunnerApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ImportRunnerApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_import_status**](ImportRunnerApi.md#get_import_status) | **GET** /api/v1/import/{job_id} | 
[**start_import**](ImportRunnerApi.md#start_import) | **POST** /api/v1/import/start | 
[**test_import_connection**](ImportRunnerApi.md#test_import_connection) | **POST** /api/v1/import/test | 


# **get_import_status**
> ImportJobStatus get_import_status(job_id => $job_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ImportRunnerApi;
my $api_instance = WWW::OpenAPIClient::ImportRunnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $job_id = "job_id_example"; # string | 

eval {
    my $result = $api_instance->get_import_status(job_id => $job_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ImportRunnerApi->get_import_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_id** | **string**|  | 

### Return type

[**ImportJobStatus**](ImportJobStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **start_import**
> ImportStartResponse start_import(import_start_request => $import_start_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ImportRunnerApi;
my $api_instance = WWW::OpenAPIClient::ImportRunnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $import_start_request = WWW::OpenAPIClient::Object::ImportStartRequest->new(); # ImportStartRequest | 

eval {
    my $result = $api_instance->start_import(import_start_request => $import_start_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ImportRunnerApi->start_import: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **import_start_request** | [**ImportStartRequest**](ImportStartRequest.md)|  | 

### Return type

[**ImportStartResponse**](ImportStartResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **test_import_connection**
> ImportTestResponse test_import_connection(import_test_request => $import_test_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ImportRunnerApi;
my $api_instance = WWW::OpenAPIClient::ImportRunnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $import_test_request = WWW::OpenAPIClient::Object::ImportTestRequest->new(); # ImportTestRequest | 

eval {
    my $result = $api_instance->test_import_connection(import_test_request => $import_test_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ImportRunnerApi->test_import_connection: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **import_test_request** | [**ImportTestRequest**](ImportTestRequest.md)|  | 

### Return type

[**ImportTestResponse**](ImportTestResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

