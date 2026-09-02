# WWW::OpenAPIClient::ProductVariantApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ProductVariantApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_product_variant**](ProductVariantApi.md#create_product_variant) | **POST** /api/v1/product-variants | 
[**delete_product_variant**](ProductVariantApi.md#delete_product_variant) | **DELETE** /api/v1/product-variants/{variant_id} | 
[**generate_product_variants**](ProductVariantApi.md#generate_product_variants) | **POST** /api/v1/product-variants/generate | 
[**get_product_variant**](ProductVariantApi.md#get_product_variant) | **GET** /api/v1/product-variants/{variant_id} | 
[**list_product_variants**](ProductVariantApi.md#list_product_variants) | **GET** /api/v1/product-variants/ | 
[**update_product_variant**](ProductVariantApi.md#update_product_variant) | **PUT** /api/v1/product-variants/{variant_id} | 


# **create_product_variant**
> ProductVariant create_product_variant(product_variant => $product_variant)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductVariantApi;
my $api_instance = WWW::OpenAPIClient::ProductVariantApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $product_variant = WWW::OpenAPIClient::Object::ProductVariant->new(); # ProductVariant | 

eval {
    my $result = $api_instance->create_product_variant(product_variant => $product_variant);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductVariantApi->create_product_variant: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **product_variant** | [**ProductVariant**](ProductVariant.md)|  | 

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_product_variant**
> delete_product_variant(variant_id => $variant_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductVariantApi;
my $api_instance = WWW::OpenAPIClient::ProductVariantApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $variant_id = "variant_id_example"; # string | 

eval {
    $api_instance->delete_product_variant(variant_id => $variant_id);
};
if ($@) {
    warn "Exception when calling ProductVariantApi->delete_product_variant: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **variant_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_product_variants**
> ARRAY[ProductVariant] generate_product_variants(generate_variants_request => $generate_variants_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductVariantApi;
my $api_instance = WWW::OpenAPIClient::ProductVariantApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $generate_variants_request = WWW::OpenAPIClient::Object::GenerateVariantsRequest->new(); # GenerateVariantsRequest | 

eval {
    my $result = $api_instance->generate_product_variants(generate_variants_request => $generate_variants_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductVariantApi->generate_product_variants: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **generate_variants_request** | [**GenerateVariantsRequest**](GenerateVariantsRequest.md)|  | 

### Return type

[**ARRAY[ProductVariant]**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_product_variant**
> ProductVariant get_product_variant(variant_id => $variant_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductVariantApi;
my $api_instance = WWW::OpenAPIClient::ProductVariantApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $variant_id = "variant_id_example"; # string | 

eval {
    my $result = $api_instance->get_product_variant(variant_id => $variant_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductVariantApi->get_product_variant: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **variant_id** | **string**|  | 

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_product_variants**
> ARRAY[ProductVariant] list_product_variants(page => $page, page_size => $page_size, product_id => $product_id, is_active => $is_active)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductVariantApi;
my $api_instance = WWW::OpenAPIClient::ProductVariantApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $product_id = "product_id_example"; # string | 
my $is_active = null; # boolean | 

eval {
    my $result = $api_instance->list_product_variants(page => $page, page_size => $page_size, product_id => $product_id, is_active => $is_active);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductVariantApi->list_product_variants: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **product_id** | **string**|  | [optional] 
 **is_active** | **boolean**|  | [optional] 

### Return type

[**ARRAY[ProductVariant]**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_product_variant**
> ProductVariant update_product_variant(variant_id => $variant_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ProductVariantApi;
my $api_instance = WWW::OpenAPIClient::ProductVariantApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $variant_id = "variant_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_product_variant(variant_id => $variant_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ProductVariantApi->update_product_variant: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **variant_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**ProductVariant**](ProductVariant.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

