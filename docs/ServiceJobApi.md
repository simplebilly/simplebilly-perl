# WWW::OpenAPIClient::ServiceJobApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ServiceJobApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_service_job**](ServiceJobApi.md#create_service_job) | **POST** /api/v1/service-jobs | 
[**delete_service_job**](ServiceJobApi.md#delete_service_job) | **DELETE** /api/v1/service-jobs/{id} | 
[**get_service_job**](ServiceJobApi.md#get_service_job) | **GET** /api/v1/service-jobs/{id} | 
[**get_service_jobs**](ServiceJobApi.md#get_service_jobs) | **GET** /api/v1/service-jobs/ | 
[**update_service_job**](ServiceJobApi.md#update_service_job) | **PUT** /api/v1/service-jobs/{id} | 


# **create_service_job**
> ServiceJob create_service_job(service_job_create => $service_job_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceJobApi;
my $api_instance = WWW::OpenAPIClient::ServiceJobApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $service_job_create = WWW::OpenAPIClient::Object::ServiceJobCreate->new(); # ServiceJobCreate | 

eval {
    my $result = $api_instance->create_service_job(service_job_create => $service_job_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceJobApi->create_service_job: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_job_create** | [**ServiceJobCreate**](ServiceJobCreate.md)|  | 

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_service_job**
> delete_service_job(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceJobApi;
my $api_instance = WWW::OpenAPIClient::ServiceJobApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_service_job(id => $id);
};
if ($@) {
    warn "Exception when calling ServiceJobApi->delete_service_job: $@\n";
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

# **get_service_job**
> ServiceJob get_service_job(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceJobApi;
my $api_instance = WWW::OpenAPIClient::ServiceJobApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_service_job(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceJobApi->get_service_job: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_service_jobs**
> ARRAY[ServiceJob] get_service_jobs(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceJobApi;
my $api_instance = WWW::OpenAPIClient::ServiceJobApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_service_jobs(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceJobApi->get_service_jobs: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **include_deleted** | **boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**ARRAY[ServiceJob]**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_service_job**
> ServiceJob update_service_job(id => $id, service_job_update => $service_job_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceJobApi;
my $api_instance = WWW::OpenAPIClient::ServiceJobApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $service_job_update = WWW::OpenAPIClient::Object::ServiceJobUpdate->new(); # ServiceJobUpdate | 

eval {
    my $result = $api_instance->update_service_job(id => $id, service_job_update => $service_job_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceJobApi->update_service_job: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **service_job_update** | [**ServiceJobUpdate**](ServiceJobUpdate.md)|  | 

### Return type

[**ServiceJob**](ServiceJob.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

