# WWW::OpenAPIClient::ServiceAssignmentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ServiceAssignmentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_service_assignment**](ServiceAssignmentApi.md#create_service_assignment) | **POST** /api/v1/service-assignments | 
[**delete_service_assignment**](ServiceAssignmentApi.md#delete_service_assignment) | **DELETE** /api/v1/service-assignments/{id} | 
[**get_service_assignment**](ServiceAssignmentApi.md#get_service_assignment) | **GET** /api/v1/service-assignments/{id} | 
[**get_service_assignments**](ServiceAssignmentApi.md#get_service_assignments) | **GET** /api/v1/service-assignments/ | 
[**update_service_assignment**](ServiceAssignmentApi.md#update_service_assignment) | **PUT** /api/v1/service-assignments/{id} | 


# **create_service_assignment**
> ServiceAssignment create_service_assignment(service_assignment_create => $service_assignment_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceAssignmentApi;
my $api_instance = WWW::OpenAPIClient::ServiceAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $service_assignment_create = WWW::OpenAPIClient::Object::ServiceAssignmentCreate->new(); # ServiceAssignmentCreate | 

eval {
    my $result = $api_instance->create_service_assignment(service_assignment_create => $service_assignment_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceAssignmentApi->create_service_assignment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **service_assignment_create** | [**ServiceAssignmentCreate**](ServiceAssignmentCreate.md)|  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_service_assignment**
> delete_service_assignment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceAssignmentApi;
my $api_instance = WWW::OpenAPIClient::ServiceAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_service_assignment(id => $id);
};
if ($@) {
    warn "Exception when calling ServiceAssignmentApi->delete_service_assignment: $@\n";
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

# **get_service_assignment**
> ServiceAssignment get_service_assignment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceAssignmentApi;
my $api_instance = WWW::OpenAPIClient::ServiceAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_service_assignment(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceAssignmentApi->get_service_assignment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_service_assignments**
> ARRAY[ServiceAssignment] get_service_assignments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceAssignmentApi;
my $api_instance = WWW::OpenAPIClient::ServiceAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_service_assignments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceAssignmentApi->get_service_assignments: $@\n";
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

[**ARRAY[ServiceAssignment]**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_service_assignment**
> ServiceAssignment update_service_assignment(id => $id, service_assignment_update => $service_assignment_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ServiceAssignmentApi;
my $api_instance = WWW::OpenAPIClient::ServiceAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $service_assignment_update = WWW::OpenAPIClient::Object::ServiceAssignmentUpdate->new(); # ServiceAssignmentUpdate | 

eval {
    my $result = $api_instance->update_service_assignment(id => $id, service_assignment_update => $service_assignment_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ServiceAssignmentApi->update_service_assignment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **service_assignment_update** | [**ServiceAssignmentUpdate**](ServiceAssignmentUpdate.md)|  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

