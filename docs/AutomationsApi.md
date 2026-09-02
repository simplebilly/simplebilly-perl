# WWW::OpenAPIClient::AutomationsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AutomationsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_automations**](AutomationsApi.md#list_automations) | **GET** /api/v1/automations | 
[**trigger_automation**](AutomationsApi.md#trigger_automation) | **POST** /api/v1/automations/{key}/trigger | 
[**update_automation**](AutomationsApi.md#update_automation) | **PUT** /api/v1/automations/{key} | 


# **list_automations**
> ARRAY[AutomationDto] list_automations()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AutomationsApi;
my $api_instance = WWW::OpenAPIClient::AutomationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_automations();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AutomationsApi->list_automations: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[AutomationDto]**](AutomationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trigger_automation**
> object trigger_automation(key => $key)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AutomationsApi;
my $api_instance = WWW::OpenAPIClient::AutomationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $key = "key_example"; # string | 

eval {
    my $result = $api_instance->trigger_automation(key => $key);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AutomationsApi->trigger_automation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_automation**
> AutomationDto update_automation(key => $key, update_automation => $update_automation)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AutomationsApi;
my $api_instance = WWW::OpenAPIClient::AutomationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $key = "key_example"; # string | 
my $update_automation = WWW::OpenAPIClient::Object::UpdateAutomation->new(); # UpdateAutomation | 

eval {
    my $result = $api_instance->update_automation(key => $key, update_automation => $update_automation);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AutomationsApi->update_automation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **key** | **string**|  | 
 **update_automation** | [**UpdateAutomation**](UpdateAutomation.md)|  | 

### Return type

[**AutomationDto**](AutomationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

