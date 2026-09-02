# WWW::OpenAPIClient::ProductCategoryApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ProductCategoryApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_product_category**](ProductCategoryApi.md#create_product_category) | **POST** /api/v1/product-categories | 
[**delete_product_category**](ProductCategoryApi.md#delete_product_category) | **DELETE** /api/v1/product-categories/{category_id} | 
[**get_product_category**](ProductCategoryApi.md#get_product_category) | **GET** /api/v1/product-categories/{category_id} | 
[**list_product_categories**](ProductCategoryApi.md#list_product_categories) | **GET** /api/v1/product-categories | 
[**update_product_category**](ProductCategoryApi.md#update_product_category) | **PUT** /api/v1/product-categories/{category_id} | 


# **create_product_category**
> ProductCategory create_product_category(product_category => $product_category)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductCategoryApi;
my $api_instance = WWW::OpenAPIClient::ProductCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_category = WWW::OpenAPIClient::Object::ProductCategory->new(); # ProductCategory | 

eval {
    my $result = $api_instance->create_product_category(product_category => $product_category);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductCategoryApi->create_product_category: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_category** | [**ProductCategory**](ProductCategory.md)|  | 

### Return type

[**ProductCategory**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_product_category**
> delete_product_category(category_id => $category_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductCategoryApi;
my $api_instance = WWW::OpenAPIClient::ProductCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $category_id = "category_id_example"; # string | 

eval {
    $api_instance->delete_product_category(category_id => $category_id);
};
if ($@) {
    warn "Exception when calling ProductCategoryApi->delete_product_category: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_product_category**
> ProductCategory get_product_category(category_id => $category_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductCategoryApi;
my $api_instance = WWW::OpenAPIClient::ProductCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $category_id = "category_id_example"; # string | 

eval {
    my $result = $api_instance->get_product_category(category_id => $category_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductCategoryApi->get_product_category: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **string**|  | 

### Return type

[**ProductCategory**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_product_categories**
> ARRAY[ProductCategory] list_product_categories()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductCategoryApi;
my $api_instance = WWW::OpenAPIClient::ProductCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_product_categories();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductCategoryApi->list_product_categories: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[ProductCategory]**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_product_category**
> ProductCategory update_product_category(category_id => $category_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductCategoryApi;
my $api_instance = WWW::OpenAPIClient::ProductCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $category_id = "category_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_product_category(category_id => $category_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductCategoryApi->update_product_category: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**ProductCategory**](ProductCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

