# WWW::OpenAPIClient::ProposeAssignmentsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ProposeAssignmentsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**propose_assignments_api**](ProposeAssignmentsApi.md#propose_assignments_api) | **GET** /api/v1/bookkeeping/propose-assignments | 


# **propose_assignments_api**
> ARRAY[ProposedAssignment] propose_assignments_api(min_confidence => $min_confidence, customer_id => $customer_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProposeAssignmentsApi;
my $api_instance = WWW::OpenAPIClient::ProposeAssignmentsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $min_confidence = 3.4; # double | 
my $customer_id = "customer_id_example"; # string | 

eval {
    my $result = $api_instance->propose_assignments_api(min_confidence => $min_confidence, customer_id => $customer_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProposeAssignmentsApi->propose_assignments_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **min_confidence** | **double**|  | [optional] 
 **customer_id** | **string**|  | [optional] 

### Return type

[**ARRAY[ProposedAssignment]**](ProposedAssignment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

