# WWW::OpenAPIClient::WorkflowsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::WorkflowsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_workflows_api**](WorkflowsApi.md#list_workflows_api) | **GET** /api/v1/workflows | 
[**set_workflow_enabled_api**](WorkflowsApi.md#set_workflow_enabled_api) | **PUT** /api/v1/workflows/{workflow_id}/enabled | 


# **list_workflows_api**
> ARRAY[Workflow] list_workflows_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WorkflowsApi;
my $api_instance = WWW::OpenAPIClient::WorkflowsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_workflows_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WorkflowsApi->list_workflows_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[Workflow]**](Workflow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_workflow_enabled_api**
> Workflow set_workflow_enabled_api(workflow_id => $workflow_id, workflow_enabled_update => $workflow_enabled_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WorkflowsApi;
my $api_instance = WWW::OpenAPIClient::WorkflowsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $workflow_id = "workflow_id_example"; # string | 
my $workflow_enabled_update = WWW::OpenAPIClient::Object::WorkflowEnabledUpdate->new(); # WorkflowEnabledUpdate | 

eval {
    my $result = $api_instance->set_workflow_enabled_api(workflow_id => $workflow_id, workflow_enabled_update => $workflow_enabled_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WorkflowsApi->set_workflow_enabled_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workflow_id** | **string**|  | 
 **workflow_enabled_update** | [**WorkflowEnabledUpdate**](WorkflowEnabledUpdate.md)|  | 

### Return type

[**Workflow**](Workflow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

