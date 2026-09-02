# WWW::OpenAPIClient::ListOpenItemsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ListOpenItemsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_open_items_api**](ListOpenItemsApi.md#list_open_items_api) | **GET** /api/v1/bookkeeping/open-items | 


# **list_open_items_api**
> ARRAY[OpenItem] list_open_items_api(reminder_level1_days => $reminder_level1_days, reminder_level2_days => $reminder_level2_days, reminder_level3_days => $reminder_level3_days, customer_id => $customer_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ListOpenItemsApi;
my $api_instance = WWW::OpenAPIClient::ListOpenItemsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $reminder_level1_days = 789; # int | 
my $reminder_level2_days = 789; # int | 
my $reminder_level3_days = 789; # int | 
my $customer_id = "customer_id_example"; # string | 

eval {
    my $result = $api_instance->list_open_items_api(reminder_level1_days => $reminder_level1_days, reminder_level2_days => $reminder_level2_days, reminder_level3_days => $reminder_level3_days, customer_id => $customer_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ListOpenItemsApi->list_open_items_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reminder_level1_days** | **int**|  | [optional] 
 **reminder_level2_days** | **int**|  | [optional] 
 **reminder_level3_days** | **int**|  | [optional] 
 **customer_id** | **string**|  | [optional] 

### Return type

[**ARRAY[OpenItem]**](OpenItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

