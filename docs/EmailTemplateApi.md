# WWW::OpenAPIClient::EmailTemplateApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::EmailTemplateApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_email_template**](EmailTemplateApi.md#create_email_template) | **POST** /api/v1/email-templates | 
[**delete_email_template**](EmailTemplateApi.md#delete_email_template) | **DELETE** /api/v1/email-templates/{email_template_id} | 
[**get_email_template**](EmailTemplateApi.md#get_email_template) | **GET** /api/v1/email-templates/{email_template_id} | 
[**list_email_templates**](EmailTemplateApi.md#list_email_templates) | **GET** /api/v1/email-templates/ | 
[**render_email_template**](EmailTemplateApi.md#render_email_template) | **POST** /api/v1/email-templates/{email_template_id}/render | 
[**update_email_template**](EmailTemplateApi.md#update_email_template) | **PUT** /api/v1/email-templates/{email_template_id} | 


# **create_email_template**
> EmailTemplate create_email_template(email_template_create => $email_template_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmailTemplateApi;
my $api_instance = WWW::OpenAPIClient::EmailTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $email_template_create = WWW::OpenAPIClient::Object::EmailTemplateCreate->new(); # EmailTemplateCreate | 

eval {
    my $result = $api_instance->create_email_template(email_template_create => $email_template_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmailTemplateApi->create_email_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_template_create** | [**EmailTemplateCreate**](EmailTemplateCreate.md)|  | 

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_email_template**
> delete_email_template(email_template_id => $email_template_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmailTemplateApi;
my $api_instance = WWW::OpenAPIClient::EmailTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $email_template_id = "email_template_id_example"; # string | 

eval {
    $api_instance->delete_email_template(email_template_id => $email_template_id);
};
if ($@) {
    warn "Exception when calling EmailTemplateApi->delete_email_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_template_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_email_template**
> EmailTemplate get_email_template(email_template_id => $email_template_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmailTemplateApi;
my $api_instance = WWW::OpenAPIClient::EmailTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $email_template_id = "email_template_id_example"; # string | 

eval {
    my $result = $api_instance->get_email_template(email_template_id => $email_template_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmailTemplateApi->get_email_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_template_id** | **string**|  | 

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_email_templates**
> ARRAY[EmailTemplate] list_email_templates(page => $page, page_size => $page_size, status => $status, search => $search)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmailTemplateApi;
my $api_instance = WWW::OpenAPIClient::EmailTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $search = "search_example"; # string | 

eval {
    my $result = $api_instance->list_email_templates(page => $page, page_size => $page_size, status => $status, search => $search);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmailTemplateApi->list_email_templates: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **search** | **string**|  | [optional] 

### Return type

[**ARRAY[EmailTemplate]**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **render_email_template**
> object render_email_template(email_template_id => $email_template_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmailTemplateApi;
my $api_instance = WWW::OpenAPIClient::EmailTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $email_template_id = "email_template_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->render_email_template(email_template_id => $email_template_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmailTemplateApi->render_email_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_template_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_email_template**
> EmailTemplate update_email_template(email_template_id => $email_template_id, email_template_update => $email_template_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmailTemplateApi;
my $api_instance = WWW::OpenAPIClient::EmailTemplateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $email_template_id = "email_template_id_example"; # string | 
my $email_template_update = WWW::OpenAPIClient::Object::EmailTemplateUpdate->new(); # EmailTemplateUpdate | 

eval {
    my $result = $api_instance->update_email_template(email_template_id => $email_template_id, email_template_update => $email_template_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmailTemplateApi->update_email_template: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email_template_id** | **string**|  | 
 **email_template_update** | [**EmailTemplateUpdate**](EmailTemplateUpdate.md)|  | 

### Return type

[**EmailTemplate**](EmailTemplate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

