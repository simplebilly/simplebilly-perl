# WWW::OpenAPIClient::ProductAttributeApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ProductAttributeApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_product_attribute**](ProductAttributeApi.md#create_product_attribute) | **POST** /api/v1/product-attributes | 
[**delete_product_attribute**](ProductAttributeApi.md#delete_product_attribute) | **DELETE** /api/v1/product-attributes/{attribute_id} | 
[**get_product_attribute**](ProductAttributeApi.md#get_product_attribute) | **GET** /api/v1/product-attributes/{attribute_id} | 
[**list_product_attributes**](ProductAttributeApi.md#list_product_attributes) | **GET** /api/v1/product-attributes/ | 
[**update_product_attribute**](ProductAttributeApi.md#update_product_attribute) | **PUT** /api/v1/product-attributes/{attribute_id} | 


# **create_product_attribute**
> ProductAttribute create_product_attribute(product_attribute_create => $product_attribute_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductAttributeApi;
my $api_instance = WWW::OpenAPIClient::ProductAttributeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_attribute_create = WWW::OpenAPIClient::Object::ProductAttributeCreate->new(); # ProductAttributeCreate | 

eval {
    my $result = $api_instance->create_product_attribute(product_attribute_create => $product_attribute_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductAttributeApi->create_product_attribute: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_attribute_create** | [**ProductAttributeCreate**](ProductAttributeCreate.md)|  | 

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_product_attribute**
> delete_product_attribute(attribute_id => $attribute_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductAttributeApi;
my $api_instance = WWW::OpenAPIClient::ProductAttributeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attribute_id = "attribute_id_example"; # string | 

eval {
    $api_instance->delete_product_attribute(attribute_id => $attribute_id);
};
if ($@) {
    warn "Exception when calling ProductAttributeApi->delete_product_attribute: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attribute_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_product_attribute**
> ProductAttribute get_product_attribute(attribute_id => $attribute_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductAttributeApi;
my $api_instance = WWW::OpenAPIClient::ProductAttributeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attribute_id = "attribute_id_example"; # string | 

eval {
    my $result = $api_instance->get_product_attribute(attribute_id => $attribute_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductAttributeApi->get_product_attribute: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attribute_id** | **string**|  | 

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_product_attributes**
> ARRAY[ProductAttribute] list_product_attributes(page => $page, page_size => $page_size, product_id => $product_id, is_filterable => $is_filterable, search => $search)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductAttributeApi;
my $api_instance = WWW::OpenAPIClient::ProductAttributeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $product_id = "product_id_example"; # string | 
my $is_filterable = null; # boolean | 
my $search = "search_example"; # string | 

eval {
    my $result = $api_instance->list_product_attributes(page => $page, page_size => $page_size, product_id => $product_id, is_filterable => $is_filterable, search => $search);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductAttributeApi->list_product_attributes: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **product_id** | **string**|  | [optional] 
 **is_filterable** | **boolean**|  | [optional] 
 **search** | **string**|  | [optional] 

### Return type

[**ARRAY[ProductAttribute]**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_product_attribute**
> ProductAttribute update_product_attribute(attribute_id => $attribute_id, product_attribute_update => $product_attribute_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductAttributeApi;
my $api_instance = WWW::OpenAPIClient::ProductAttributeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attribute_id = "attribute_id_example"; # string | 
my $product_attribute_update = WWW::OpenAPIClient::Object::ProductAttributeUpdate->new(); # ProductAttributeUpdate | 

eval {
    my $result = $api_instance->update_product_attribute(attribute_id => $attribute_id, product_attribute_update => $product_attribute_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductAttributeApi->update_product_attribute: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attribute_id** | **string**|  | 
 **product_attribute_update** | [**ProductAttributeUpdate**](ProductAttributeUpdate.md)|  | 

### Return type

[**ProductAttribute**](ProductAttribute.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

