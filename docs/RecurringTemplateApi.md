# WWW::OpenAPIClient::RecurringTemplateApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::RecurringTemplateApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_recurring_template**](RecurringTemplateApi.md#create_recurring_template) | **POST** /api/v1/recurring-templates | 
[**delete_recurring_template**](RecurringTemplateApi.md#delete_recurring_template) | **DELETE** /api/v1/recurring-templates/{template_id} | 
[**get_recurring_template**](RecurringTemplateApi.md#get_recurring_template) | **GET** /api/v1/recurring-templates/{template_id} | 
[**list_recurring_templates**](RecurringTemplateApi.md#list_recurring_templates) | **GET** /api/v1/recurring-templates/ | 


# **create_recurring_template**
> RecurringTemplate create_recurring_template(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RecurringTemplateApi;
my $api_instance = WWW::OpenAPIClient::RecurringTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->create_recurring_template(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RecurringTemplateApi->create_recurring_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**RecurringTemplate**](RecurringTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_recurring_template**
> delete_recurring_template(template_id => $template_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RecurringTemplateApi;
my $api_instance = WWW::OpenAPIClient::RecurringTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $template_id = "template_id_example"; # string | 

eval {
    $api_instance->delete_recurring_template(template_id => $template_id);
};
if ($@) {
    warn "Exception when calling RecurringTemplateApi->delete_recurring_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_recurring_template**
> RecurringTemplate get_recurring_template(template_id => $template_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RecurringTemplateApi;
my $api_instance = WWW::OpenAPIClient::RecurringTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $template_id = "template_id_example"; # string | 

eval {
    my $result = $api_instance->get_recurring_template(template_id => $template_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RecurringTemplateApi->get_recurring_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **template_id** | **string**|  | 

### Return type

[**RecurringTemplate**](RecurringTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_recurring_templates**
> ARRAY[RecurringTemplate] list_recurring_templates()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RecurringTemplateApi;
my $api_instance = WWW::OpenAPIClient::RecurringTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_recurring_templates();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RecurringTemplateApi->list_recurring_templates: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[RecurringTemplate]**](RecurringTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

