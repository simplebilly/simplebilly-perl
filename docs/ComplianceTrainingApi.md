# WWW::OpenAPIClient::ComplianceTrainingApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ComplianceTrainingApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_compliance_training**](ComplianceTrainingApi.md#create_compliance_training) | **POST** /api/v1/compliance-trainings | 
[**delete_compliance_training**](ComplianceTrainingApi.md#delete_compliance_training) | **DELETE** /api/v1/compliance-trainings/{id} | 
[**get_compliance_training**](ComplianceTrainingApi.md#get_compliance_training) | **GET** /api/v1/compliance-trainings/{id} | 
[**get_compliance_trainings**](ComplianceTrainingApi.md#get_compliance_trainings) | **GET** /api/v1/compliance-trainings/ | 
[**update_compliance_training**](ComplianceTrainingApi.md#update_compliance_training) | **PUT** /api/v1/compliance-trainings/{id} | 


# **create_compliance_training**
> ComplianceTraining create_compliance_training(compliance_training_create => $compliance_training_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ComplianceTrainingApi;
my $api_instance = WWW::OpenAPIClient::ComplianceTrainingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $compliance_training_create = WWW::OpenAPIClient::Object::ComplianceTrainingCreate->new(); # ComplianceTrainingCreate | 

eval {
    my $result = $api_instance->create_compliance_training(compliance_training_create => $compliance_training_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ComplianceTrainingApi->create_compliance_training: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **compliance_training_create** | [**ComplianceTrainingCreate**](ComplianceTrainingCreate.md)|  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_compliance_training**
> delete_compliance_training(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ComplianceTrainingApi;
my $api_instance = WWW::OpenAPIClient::ComplianceTrainingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_compliance_training(id => $id);
};
if ($@) {
    warn "Exception when calling ComplianceTrainingApi->delete_compliance_training: $@\n";
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

# **get_compliance_training**
> ComplianceTraining get_compliance_training(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ComplianceTrainingApi;
my $api_instance = WWW::OpenAPIClient::ComplianceTrainingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_compliance_training(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ComplianceTrainingApi->get_compliance_training: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_compliance_trainings**
> ARRAY[ComplianceTraining] get_compliance_trainings(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ComplianceTrainingApi;
my $api_instance = WWW::OpenAPIClient::ComplianceTrainingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_compliance_trainings(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ComplianceTrainingApi->get_compliance_trainings: $@\n";
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

[**ARRAY[ComplianceTraining]**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_compliance_training**
> ComplianceTraining update_compliance_training(id => $id, compliance_training_update => $compliance_training_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ComplianceTrainingApi;
my $api_instance = WWW::OpenAPIClient::ComplianceTrainingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $compliance_training_update = WWW::OpenAPIClient::Object::ComplianceTrainingUpdate->new(); # ComplianceTrainingUpdate | 

eval {
    my $result = $api_instance->update_compliance_training(id => $id, compliance_training_update => $compliance_training_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ComplianceTrainingApi->update_compliance_training: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **compliance_training_update** | [**ComplianceTrainingUpdate**](ComplianceTrainingUpdate.md)|  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

