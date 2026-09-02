# WWW::OpenAPIClient::SupplierConditionApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::SupplierConditionApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_supplier_condition**](SupplierConditionApi.md#create_supplier_condition) | **POST** /api/v1/supplier-conditions | 
[**delete_supplier_condition**](SupplierConditionApi.md#delete_supplier_condition) | **DELETE** /api/v1/supplier-conditions/{supplier_condition_id} | 
[**get_supplier_condition**](SupplierConditionApi.md#get_supplier_condition) | **GET** /api/v1/supplier-conditions/{supplier_condition_id} | 
[**list_supplier_conditions**](SupplierConditionApi.md#list_supplier_conditions) | **GET** /api/v1/supplier-conditions/ | 
[**update_supplier_condition**](SupplierConditionApi.md#update_supplier_condition) | **PUT** /api/v1/supplier-conditions/{supplier_condition_id} | 


# **create_supplier_condition**
> SupplierCondition create_supplier_condition(supplier_condition_create => $supplier_condition_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierConditionApi;
my $api_instance = WWW::OpenAPIClient::SupplierConditionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_condition_create = WWW::OpenAPIClient::Object::SupplierConditionCreate->new(); # SupplierConditionCreate | 

eval {
    my $result = $api_instance->create_supplier_condition(supplier_condition_create => $supplier_condition_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierConditionApi->create_supplier_condition: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_condition_create** | [**SupplierConditionCreate**](SupplierConditionCreate.md)|  | 

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_supplier_condition**
> delete_supplier_condition(supplier_condition_id => $supplier_condition_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierConditionApi;
my $api_instance = WWW::OpenAPIClient::SupplierConditionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_condition_id = "supplier_condition_id_example"; # string | 

eval {
    $api_instance->delete_supplier_condition(supplier_condition_id => $supplier_condition_id);
};
if ($@) {
    warn "Exception when calling SupplierConditionApi->delete_supplier_condition: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_condition_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_supplier_condition**
> SupplierCondition get_supplier_condition(supplier_condition_id => $supplier_condition_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierConditionApi;
my $api_instance = WWW::OpenAPIClient::SupplierConditionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_condition_id = "supplier_condition_id_example"; # string | 

eval {
    my $result = $api_instance->get_supplier_condition(supplier_condition_id => $supplier_condition_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierConditionApi->get_supplier_condition: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_condition_id** | **string**|  | 

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_supplier_conditions**
> ARRAY[SupplierCondition] list_supplier_conditions(page => $page, page_size => $page_size, supplier_contact_id => $supplier_contact_id, search => $search)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierConditionApi;
my $api_instance = WWW::OpenAPIClient::SupplierConditionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $supplier_contact_id = "supplier_contact_id_example"; # string | 
my $search = "search_example"; # string | 

eval {
    my $result = $api_instance->list_supplier_conditions(page => $page, page_size => $page_size, supplier_contact_id => $supplier_contact_id, search => $search);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierConditionApi->list_supplier_conditions: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **supplier_contact_id** | **string**|  | [optional] 
 **search** | **string**|  | [optional] 

### Return type

[**ARRAY[SupplierCondition]**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_supplier_condition**
> SupplierCondition update_supplier_condition(supplier_condition_id => $supplier_condition_id, supplier_condition_update => $supplier_condition_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupplierConditionApi;
my $api_instance = WWW::OpenAPIClient::SupplierConditionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $supplier_condition_id = "supplier_condition_id_example"; # string | 
my $supplier_condition_update = WWW::OpenAPIClient::Object::SupplierConditionUpdate->new(); # SupplierConditionUpdate | 

eval {
    my $result = $api_instance->update_supplier_condition(supplier_condition_id => $supplier_condition_id, supplier_condition_update => $supplier_condition_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupplierConditionApi->update_supplier_condition: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **supplier_condition_id** | **string**|  | 
 **supplier_condition_update** | [**SupplierConditionUpdate**](SupplierConditionUpdate.md)|  | 

### Return type

[**SupplierCondition**](SupplierCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

