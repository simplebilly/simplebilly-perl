# WWW::OpenAPIClient::TrainingAssignmentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::TrainingAssignmentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_training_assignment**](TrainingAssignmentApi.md#create_training_assignment) | **POST** /api/v1/training-assignments | 
[**delete_training_assignment**](TrainingAssignmentApi.md#delete_training_assignment) | **DELETE** /api/v1/training-assignments/{id} | 
[**get_training_assignment**](TrainingAssignmentApi.md#get_training_assignment) | **GET** /api/v1/training-assignments/{id} | 
[**get_training_assignments**](TrainingAssignmentApi.md#get_training_assignments) | **GET** /api/v1/training-assignments/ | 
[**update_training_assignment**](TrainingAssignmentApi.md#update_training_assignment) | **PUT** /api/v1/training-assignments/{id} | 


# **create_training_assignment**
> TrainingAssignment create_training_assignment(training_assignment_create => $training_assignment_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingAssignmentApi;
my $api_instance = WWW::OpenAPIClient::TrainingAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $training_assignment_create = WWW::OpenAPIClient::Object::TrainingAssignmentCreate->new(); # TrainingAssignmentCreate | 

eval {
    my $result = $api_instance->create_training_assignment(training_assignment_create => $training_assignment_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingAssignmentApi->create_training_assignment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **training_assignment_create** | [**TrainingAssignmentCreate**](TrainingAssignmentCreate.md)|  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_training_assignment**
> delete_training_assignment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingAssignmentApi;
my $api_instance = WWW::OpenAPIClient::TrainingAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_training_assignment(id => $id);
};
if ($@) {
    warn "Exception when calling TrainingAssignmentApi->delete_training_assignment: $@\n";
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

# **get_training_assignment**
> TrainingAssignment get_training_assignment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingAssignmentApi;
my $api_instance = WWW::OpenAPIClient::TrainingAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_training_assignment(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingAssignmentApi->get_training_assignment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_training_assignments**
> ARRAY[TrainingAssignment] get_training_assignments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingAssignmentApi;
my $api_instance = WWW::OpenAPIClient::TrainingAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_training_assignments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingAssignmentApi->get_training_assignments: $@\n";
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

[**ARRAY[TrainingAssignment]**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_training_assignment**
> TrainingAssignment update_training_assignment(id => $id, training_assignment_update => $training_assignment_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingAssignmentApi;
my $api_instance = WWW::OpenAPIClient::TrainingAssignmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $training_assignment_update = WWW::OpenAPIClient::Object::TrainingAssignmentUpdate->new(); # TrainingAssignmentUpdate | 

eval {
    my $result = $api_instance->update_training_assignment(id => $id, training_assignment_update => $training_assignment_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingAssignmentApi->update_training_assignment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **training_assignment_update** | [**TrainingAssignmentUpdate**](TrainingAssignmentUpdate.md)|  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

