# WWW::OpenAPIClient::LeadApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::LeadApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_leads_api**](LeadApi.md#list_leads_api) | **GET** /api/v1/support/leads | 
[**update_lead_api**](LeadApi.md#update_lead_api) | **PUT** /api/v1/support/leads/{lead_id} | 


# **list_leads_api**
> ARRAY[Lead] list_leads_api(status => $status, source => $source, search => $search, page => $page, page_size => $page_size)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::LeadApi;
my $api_instance = WWW::OpenAPIClient::LeadApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $status = "status_example"; # string | 
my $source = "source_example"; # string | 
my $search = "search_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->list_leads_api(status => $status, source => $source, search => $search, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling LeadApi->list_leads_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **string**|  | [optional] 
 **source** | **string**|  | [optional] 
 **search** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**ARRAY[Lead]**](Lead.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_lead_api**
> Lead update_lead_api(lead_id => $lead_id, lead_update => $lead_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::LeadApi;
my $api_instance = WWW::OpenAPIClient::LeadApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $lead_id = "lead_id_example"; # string | 
my $lead_update = WWW::OpenAPIClient::Object::LeadUpdate->new(); # LeadUpdate | 

eval {
    my $result = $api_instance->update_lead_api(lead_id => $lead_id, lead_update => $lead_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling LeadApi->update_lead_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **lead_id** | **string**|  | 
 **lead_update** | [**LeadUpdate**](LeadUpdate.md)|  | 

### Return type

[**Lead**](Lead.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

