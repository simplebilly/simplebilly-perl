# WWW::OpenAPIClient::CustomerApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::CustomerApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_customer**](CustomerApi.md#create_customer) | **POST** /api/v1/customers | 
[**customer_restore**](CustomerApi.md#customer_restore) | **POST** /api/v1/customers/{customer_id}/restore | 
[**delete_customer**](CustomerApi.md#delete_customer) | **DELETE** /api/v1/customers/{customer_id} | 
[**get_customer**](CustomerApi.md#get_customer) | **GET** /api/v1/customers/{customer_id} | 
[**get_customers**](CustomerApi.md#get_customers) | **GET** /api/v1/customers/ | 
[**update_customer**](CustomerApi.md#update_customer) | **PUT** /api/v1/customers/{customer_id} | 


# **create_customer**
> Customer create_customer(customer_create => $customer_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerApi;
my $api_instance = WWW::OpenAPIClient::CustomerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_create = WWW::OpenAPIClient::Object::CustomerCreate->new(); # CustomerCreate | 

eval {
    my $result = $api_instance->create_customer(customer_create => $customer_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerApi->create_customer: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_create** | [**CustomerCreate**](CustomerCreate.md)|  | 

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **customer_restore**
> Customer customer_restore(customer_id => $customer_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerApi;
my $api_instance = WWW::OpenAPIClient::CustomerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_id = "customer_id_example"; # string | 

eval {
    my $result = $api_instance->customer_restore(customer_id => $customer_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerApi->customer_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_id** | **string**|  | 

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_customer**
> delete_customer(customer_id => $customer_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerApi;
my $api_instance = WWW::OpenAPIClient::CustomerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_id = "customer_id_example"; # string | 

eval {
    $api_instance->delete_customer(customer_id => $customer_id);
};
if ($@) {
    warn "Exception when calling CustomerApi->delete_customer: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_customer**
> Customer get_customer(customer_id => $customer_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerApi;
my $api_instance = WWW::OpenAPIClient::CustomerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_id = "customer_id_example"; # string | 

eval {
    my $result = $api_instance->get_customer(customer_id => $customer_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerApi->get_customer: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_id** | **string**|  | 

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_customers**
> ARRAY[Customer] get_customers(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerApi;
my $api_instance = WWW::OpenAPIClient::CustomerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_customers(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerApi->get_customers: $@\n";
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

[**ARRAY[Customer]**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_customer**
> Customer update_customer(customer_id => $customer_id, customer_update => $customer_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerApi;
my $api_instance = WWW::OpenAPIClient::CustomerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_id = "customer_id_example"; # string | 
my $customer_update = WWW::OpenAPIClient::Object::CustomerUpdate->new(); # CustomerUpdate | 

eval {
    my $result = $api_instance->update_customer(customer_id => $customer_id, customer_update => $customer_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerApi->update_customer: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_id** | **string**|  | 
 **customer_update** | [**CustomerUpdate**](CustomerUpdate.md)|  | 

### Return type

[**Customer**](Customer.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

