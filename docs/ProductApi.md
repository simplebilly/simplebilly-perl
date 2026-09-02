# WWW::OpenAPIClient::ProductApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ProductApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_product_api**](ProductApi.md#create_product_api) | **POST** /api/v1/products | 
[**delete_product_api**](ProductApi.md#delete_product_api) | **DELETE** /api/v1/products/{product_id} | 
[**get_product_api**](ProductApi.md#get_product_api) | **GET** /api/v1/products/{product_id} | 
[**get_product_stock_api**](ProductApi.md#get_product_stock_api) | **GET** /api/v1/products/{product_id}/stock | 
[**get_products_api**](ProductApi.md#get_products_api) | **GET** /api/v1/products/ | 
[**list_low_stock_products_api**](ProductApi.md#list_low_stock_products_api) | **GET** /api/v1/products/low-stock | 
[**product_restore**](ProductApi.md#product_restore) | **POST** /api/v1/products/{product_id}/restore | 
[**update_product_api**](ProductApi.md#update_product_api) | **PUT** /api/v1/products/{product_id} | 
[**update_product_stock_api**](ProductApi.md#update_product_stock_api) | **PUT** /api/v1/products/{product_id}/stock | 


# **create_product_api**
> Product create_product_api(product_create => $product_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_create = WWW::OpenAPIClient::Object::ProductCreate->new(); # ProductCreate | 

eval {
    my $result = $api_instance->create_product_api(product_create => $product_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->create_product_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_create** | [**ProductCreate**](ProductCreate.md)|  | 

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_product_api**
> delete_product_api(product_id => $product_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 

eval {
    $api_instance->delete_product_api(product_id => $product_id);
};
if ($@) {
    warn "Exception when calling ProductApi->delete_product_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_product_api**
> Product get_product_api(product_id => $product_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 

eval {
    my $result = $api_instance->get_product_api(product_id => $product_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->get_product_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_product_stock_api**
> ProductStock get_product_stock_api(product_id => $product_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 

eval {
    my $result = $api_instance->get_product_stock_api(product_id => $product_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->get_product_stock_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 

### Return type

[**ProductStock**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_products_api**
> ARRAY[Product] get_products_api(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_products_api(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->get_products_api: $@\n";
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

[**ARRAY[Product]**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_low_stock_products_api**
> ARRAY[ProductStock] list_low_stock_products_api(threshold => $threshold)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $threshold = 789; # int | 

eval {
    my $result = $api_instance->list_low_stock_products_api(threshold => $threshold);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->list_low_stock_products_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **threshold** | **int**|  | [optional] 

### Return type

[**ARRAY[ProductStock]**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **product_restore**
> Product product_restore(product_id => $product_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 

eval {
    my $result = $api_instance->product_restore(product_id => $product_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->product_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_product_api**
> Product update_product_api(product_id => $product_id, product_update => $product_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 
my $product_update = WWW::OpenAPIClient::Object::ProductUpdate->new(); # ProductUpdate | 

eval {
    my $result = $api_instance->update_product_api(product_id => $product_id, product_update => $product_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->update_product_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 
 **product_update** | [**ProductUpdate**](ProductUpdate.md)|  | 

### Return type

[**Product**](Product.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_product_stock_api**
> ProductStock update_product_stock_api(product_id => $product_id, stock_update_request => $stock_update_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductApi;
my $api_instance = WWW::OpenAPIClient::ProductApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_id = "product_id_example"; # string | 
my $stock_update_request = WWW::OpenAPIClient::Object::StockUpdateRequest->new(); # StockUpdateRequest | 

eval {
    my $result = $api_instance->update_product_stock_api(product_id => $product_id, stock_update_request => $stock_update_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductApi->update_product_stock_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_id** | **string**|  | 
 **stock_update_request** | [**StockUpdateRequest**](StockUpdateRequest.md)|  | 

### Return type

[**ProductStock**](ProductStock.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

