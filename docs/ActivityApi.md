# WWW::OpenAPIClient::ActivityApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ActivityApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_activity**](ActivityApi.md#create_activity) | **POST** /api/v1/activities | 
[**delete_activity**](ActivityApi.md#delete_activity) | **DELETE** /api/v1/activities/{activity_id} | 
[**get_activity**](ActivityApi.md#get_activity) | **GET** /api/v1/activities/{activity_id} | 
[**list_activities**](ActivityApi.md#list_activities) | **GET** /api/v1/activities/ | 
[**update_activity**](ActivityApi.md#update_activity) | **PUT** /api/v1/activities/{activity_id} | 
[**update_activity_status**](ActivityApi.md#update_activity_status) | **PUT** /api/v1/activities/{activity_id}/status | 


# **create_activity**
> Activity create_activity(activity => $activity)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ActivityApi;
my $api_instance = WWW::OpenAPIClient::ActivityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $activity = WWW::OpenAPIClient::Object::Activity->new(); # Activity | 

eval {
    my $result = $api_instance->create_activity(activity => $activity);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ActivityApi->create_activity: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activity** | [**Activity**](Activity.md)|  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_activity**
> delete_activity(activity_id => $activity_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ActivityApi;
my $api_instance = WWW::OpenAPIClient::ActivityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $activity_id = "activity_id_example"; # string | 

eval {
    $api_instance->delete_activity(activity_id => $activity_id);
};
if ($@) {
    warn "Exception when calling ActivityApi->delete_activity: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activity_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_activity**
> Activity get_activity(activity_id => $activity_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ActivityApi;
my $api_instance = WWW::OpenAPIClient::ActivityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $activity_id = "activity_id_example"; # string | 

eval {
    my $result = $api_instance->get_activity(activity_id => $activity_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ActivityApi->get_activity: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activity_id** | **string**|  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_activities**
> ARRAY[Activity] list_activities(page => $page, page_size => $page_size, contact_id => $contact_id, activity_type => $activity_type, status => $status, assigned_to => $assigned_to, overdue_only => $overdue_only)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ActivityApi;
my $api_instance = WWW::OpenAPIClient::ActivityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $contact_id = "contact_id_example"; # string | 
my $activity_type = "activity_type_example"; # string | 
my $status = "status_example"; # string | 
my $assigned_to = "assigned_to_example"; # string | 
my $overdue_only = null; # boolean | Only show overdue follow-ups.

eval {
    my $result = $api_instance->list_activities(page => $page, page_size => $page_size, contact_id => $contact_id, activity_type => $activity_type, status => $status, assigned_to => $assigned_to, overdue_only => $overdue_only);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ActivityApi->list_activities: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **contact_id** | **string**|  | [optional] 
 **activity_type** | **string**|  | [optional] 
 **status** | **string**|  | [optional] 
 **assigned_to** | **string**|  | [optional] 
 **overdue_only** | **boolean**| Only show overdue follow-ups. | [optional] 

### Return type

[**ARRAY[Activity]**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_activity**
> Activity update_activity(activity_id => $activity_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ActivityApi;
my $api_instance = WWW::OpenAPIClient::ActivityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $activity_id = "activity_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_activity(activity_id => $activity_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ActivityApi->update_activity: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activity_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_activity_status**
> Activity update_activity_status(activity_id => $activity_id, activity_status_update => $activity_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ActivityApi;
my $api_instance = WWW::OpenAPIClient::ActivityApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $activity_id = "activity_id_example"; # string | 
my $activity_status_update = WWW::OpenAPIClient::Object::ActivityStatusUpdate->new(); # ActivityStatusUpdate | 

eval {
    my $result = $api_instance->update_activity_status(activity_id => $activity_id, activity_status_update => $activity_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ActivityApi->update_activity_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **activity_id** | **string**|  | 
 **activity_status_update** | [**ActivityStatusUpdate**](ActivityStatusUpdate.md)|  | 

### Return type

[**Activity**](Activity.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

