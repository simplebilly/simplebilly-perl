# WWW::OpenAPIClient::JobPostingApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::JobPostingApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_job_posting**](JobPostingApi.md#create_job_posting) | **POST** /api/v1/job-postings | 
[**delete_job_posting**](JobPostingApi.md#delete_job_posting) | **DELETE** /api/v1/job-postings/{id} | 
[**get_job_posting**](JobPostingApi.md#get_job_posting) | **GET** /api/v1/job-postings/{id} | 
[**list_job_postings**](JobPostingApi.md#list_job_postings) | **GET** /api/v1/job-postings | 
[**update_job_posting**](JobPostingApi.md#update_job_posting) | **PUT** /api/v1/job-postings/{id} | 


# **create_job_posting**
> JobPosting create_job_posting(job_posting_create => $job_posting_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobPostingApi;
my $api_instance = WWW::OpenAPIClient::JobPostingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $job_posting_create = WWW::OpenAPIClient::Object::JobPostingCreate->new(); # JobPostingCreate | 

eval {
    my $result = $api_instance->create_job_posting(job_posting_create => $job_posting_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobPostingApi->create_job_posting: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **job_posting_create** | [**JobPostingCreate**](JobPostingCreate.md)|  | 

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_job_posting**
> delete_job_posting(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobPostingApi;
my $api_instance = WWW::OpenAPIClient::JobPostingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_job_posting(id => $id);
};
if ($@) {
    warn "Exception when calling JobPostingApi->delete_job_posting: $@\n";
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

# **get_job_posting**
> JobPosting get_job_posting(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobPostingApi;
my $api_instance = WWW::OpenAPIClient::JobPostingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_job_posting(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobPostingApi->get_job_posting: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_job_postings**
> ARRAY[JobPosting] list_job_postings(status => $status, page => $page, page_size => $page_size)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobPostingApi;
my $api_instance = WWW::OpenAPIClient::JobPostingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $status = "status_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->list_job_postings(status => $status, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobPostingApi->list_job_postings: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**ARRAY[JobPosting]**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_job_posting**
> JobPosting update_job_posting(id => $id, job_posting_update => $job_posting_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobPostingApi;
my $api_instance = WWW::OpenAPIClient::JobPostingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $job_posting_update = WWW::OpenAPIClient::Object::JobPostingUpdate->new(); # JobPostingUpdate | 

eval {
    my $result = $api_instance->update_job_posting(id => $id, job_posting_update => $job_posting_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobPostingApi->update_job_posting: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **job_posting_update** | [**JobPostingUpdate**](JobPostingUpdate.md)|  | 

### Return type

[**JobPosting**](JobPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

