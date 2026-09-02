# WWW::OpenAPIClient::JobApplicationApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::JobApplicationApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apply_public**](JobApplicationApi.md#apply_public) | **POST** /api/v1/public/jobs/{posting_id}/apply | 
[**delete_job_application**](JobApplicationApi.md#delete_job_application) | **DELETE** /api/v1/job-applications/{application_id} | 
[**download_cv**](JobApplicationApi.md#download_cv) | **GET** /api/v1/job-applications/{application_id}/cv | 
[**get_job_application**](JobApplicationApi.md#get_job_application) | **GET** /api/v1/job-applications/{application_id} | 
[**inbound_email**](JobApplicationApi.md#inbound_email) | **POST** /api/v1/public/jobs/inbound-email | Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with &#x60;from&#x60;, &#x60;subject&#x60;, &#x60;body-plain&#x60; and one or more &#x60;attachment-N&#x60; file fields. The subject may reference a posting as &#x60;[JOB-&lt;posting_id&gt;]&#x60;; without one the application lands in the general inbox.
[**list_job_applications**](JobApplicationApi.md#list_job_applications) | **GET** /api/v1/job-applications | 
[**list_public_postings**](JobApplicationApi.md#list_public_postings) | **GET** /api/v1/public/jobs | 
[**score_job_application**](JobApplicationApi.md#score_job_application) | **POST** /api/v1/job-applications/{application_id}/score | 
[**update_job_application_status**](JobApplicationApi.md#update_job_application_status) | **PATCH** /api/v1/job-applications/{application_id}/status | 


# **apply_public**
> apply_public(posting_id => $posting_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $posting_id = "posting_id_example"; # string | 

eval {
    $api_instance->apply_public(posting_id => $posting_id);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->apply_public: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **posting_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_job_application**
> JobApplication delete_job_application(application_id => $application_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $application_id = "application_id_example"; # string | 

eval {
    my $result = $api_instance->delete_job_application(application_id => $application_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->delete_job_application: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **string**|  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_cv**
> download_cv(application_id => $application_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $application_id = "application_id_example"; # string | 

eval {
    $api_instance->download_cv(application_id => $application_id);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->download_cv: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_job_application**
> JobApplication get_job_application(application_id => $application_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $application_id = "application_id_example"; # string | 

eval {
    my $result = $api_instance->get_job_application(application_id => $application_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->get_job_application: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **string**|  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **inbound_email**
> inbound_email()

Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    $api_instance->inbound_email();
};
if ($@) {
    warn "Exception when calling JobApplicationApi->inbound_email: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_job_applications**
> ARRAY[JobApplication] list_job_applications(posting_id => $posting_id, status => $status, page => $page, page_size => $page_size)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $posting_id = "posting_id_example"; # string | 
my $status = "status_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->list_job_applications(posting_id => $posting_id, status => $status, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->list_job_applications: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **posting_id** | **string**|  | [optional] 
 **status** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**ARRAY[JobApplication]**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_public_postings**
> ARRAY[PublicPosting] list_public_postings()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_public_postings();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->list_public_postings: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[PublicPosting]**](PublicPosting.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **score_job_application**
> JobApplication score_job_application(application_id => $application_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $application_id = "application_id_example"; # string | 

eval {
    my $result = $api_instance->score_job_application(application_id => $application_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->score_job_application: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **string**|  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_job_application_status**
> JobApplication update_job_application_status(application_id => $application_id, application_status_dto => $application_status_dto)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::JobApplicationApi;
my $api_instance = WWW::OpenAPIClient::JobApplicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $application_id = "application_id_example"; # string | 
my $application_status_dto = WWW::OpenAPIClient::Object::ApplicationStatusDto->new(); # ApplicationStatusDto | 

eval {
    my $result = $api_instance->update_job_application_status(application_id => $application_id, application_status_dto => $application_status_dto);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling JobApplicationApi->update_job_application_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **application_id** | **string**|  | 
 **application_status_dto** | [**ApplicationStatusDto**](ApplicationStatusDto.md)|  | 

### Return type

[**JobApplication**](JobApplication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

