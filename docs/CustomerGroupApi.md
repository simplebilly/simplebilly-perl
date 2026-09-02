# WWW::OpenAPIClient::CustomerGroupApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::CustomerGroupApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_group_members**](CustomerGroupApi.md#add_group_members) | **POST** /api/v1/customer-groups/{customer_group_id}/members | 
[**create_customer_group**](CustomerGroupApi.md#create_customer_group) | **POST** /api/v1/customer-groups | 
[**delete_customer_group**](CustomerGroupApi.md#delete_customer_group) | **DELETE** /api/v1/customer-groups/{customer_group_id} | 
[**get_customer_group**](CustomerGroupApi.md#get_customer_group) | **GET** /api/v1/customer-groups/{customer_group_id} | 
[**list_customer_groups**](CustomerGroupApi.md#list_customer_groups) | **GET** /api/v1/customer-groups/ | 
[**update_customer_group**](CustomerGroupApi.md#update_customer_group) | **PUT** /api/v1/customer-groups/{customer_group_id} | 


# **add_group_members**
> CustomerGroup add_group_members(customer_group_id => $customer_group_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerGroupApi;
my $api_instance = WWW::OpenAPIClient::CustomerGroupApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_group_id = "customer_group_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->add_group_members(customer_group_id => $customer_group_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerGroupApi->add_group_members: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_group_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_customer_group**
> CustomerGroup create_customer_group(customer_group_create => $customer_group_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerGroupApi;
my $api_instance = WWW::OpenAPIClient::CustomerGroupApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_group_create = WWW::OpenAPIClient::Object::CustomerGroupCreate->new(); # CustomerGroupCreate | 

eval {
    my $result = $api_instance->create_customer_group(customer_group_create => $customer_group_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerGroupApi->create_customer_group: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_group_create** | [**CustomerGroupCreate**](CustomerGroupCreate.md)|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_customer_group**
> delete_customer_group(customer_group_id => $customer_group_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerGroupApi;
my $api_instance = WWW::OpenAPIClient::CustomerGroupApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_group_id = "customer_group_id_example"; # string | 

eval {
    $api_instance->delete_customer_group(customer_group_id => $customer_group_id);
};
if ($@) {
    warn "Exception when calling CustomerGroupApi->delete_customer_group: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_group_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_customer_group**
> CustomerGroup get_customer_group(customer_group_id => $customer_group_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerGroupApi;
my $api_instance = WWW::OpenAPIClient::CustomerGroupApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_group_id = "customer_group_id_example"; # string | 

eval {
    my $result = $api_instance->get_customer_group(customer_group_id => $customer_group_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerGroupApi->get_customer_group: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_group_id** | **string**|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_customer_groups**
> ARRAY[CustomerGroup] list_customer_groups(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerGroupApi;
my $api_instance = WWW::OpenAPIClient::CustomerGroupApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->list_customer_groups(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerGroupApi->list_customer_groups: $@\n";
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

[**ARRAY[CustomerGroup]**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_customer_group**
> CustomerGroup update_customer_group(customer_group_id => $customer_group_id, customer_group_update => $customer_group_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerGroupApi;
my $api_instance = WWW::OpenAPIClient::CustomerGroupApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_group_id = "customer_group_id_example"; # string | 
my $customer_group_update = WWW::OpenAPIClient::Object::CustomerGroupUpdate->new(); # CustomerGroupUpdate | 

eval {
    my $result = $api_instance->update_customer_group(customer_group_id => $customer_group_id, customer_group_update => $customer_group_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerGroupApi->update_customer_group: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_group_id** | **string**|  | 
 **customer_group_update** | [**CustomerGroupUpdate**](CustomerGroupUpdate.md)|  | 

### Return type

[**CustomerGroup**](CustomerGroup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

