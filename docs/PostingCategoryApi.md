# WWW::OpenAPIClient::PostingCategoryApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PostingCategoryApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_posting_category**](PostingCategoryApi.md#create_posting_category) | **POST** /api/v1/posting-categories | 
[**delete_posting_category**](PostingCategoryApi.md#delete_posting_category) | **DELETE** /api/v1/posting-categories/{category_id} | 
[**list_posting_categories**](PostingCategoryApi.md#list_posting_categories) | **GET** /api/v1/posting-categories | 
[**seed_posting_categories**](PostingCategoryApi.md#seed_posting_categories) | **POST** /api/v1/posting-categories/seed/{skr_version} | 
[**update_posting_category**](PostingCategoryApi.md#update_posting_category) | **PUT** /api/v1/posting-categories/{category_id} | 


# **create_posting_category**
> PostingCategory create_posting_category(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PostingCategoryApi;
my $api_instance = WWW::OpenAPIClient::PostingCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->create_posting_category(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PostingCategoryApi->create_posting_category: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**PostingCategory**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_posting_category**
> delete_posting_category(category_id => $category_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PostingCategoryApi;
my $api_instance = WWW::OpenAPIClient::PostingCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $category_id = "category_id_example"; # string | 

eval {
    $api_instance->delete_posting_category(category_id => $category_id);
};
if ($@) {
    warn "Exception when calling PostingCategoryApi->delete_posting_category: $@\n";
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

# **list_posting_categories**
> ARRAY[PostingCategory] list_posting_categories()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PostingCategoryApi;
my $api_instance = WWW::OpenAPIClient::PostingCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_posting_categories();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PostingCategoryApi->list_posting_categories: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[PostingCategory]**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **seed_posting_categories**
> seed_posting_categories(skr_version => $skr_version)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PostingCategoryApi;
my $api_instance = WWW::OpenAPIClient::PostingCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $skr_version = "skr_version_example"; # string | 

eval {
    $api_instance->seed_posting_categories(skr_version => $skr_version);
};
if ($@) {
    warn "Exception when calling PostingCategoryApi->seed_posting_categories: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **skr_version** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_posting_category**
> PostingCategory update_posting_category(category_id => $category_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PostingCategoryApi;
my $api_instance = WWW::OpenAPIClient::PostingCategoryApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $category_id = "category_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_posting_category(category_id => $category_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PostingCategoryApi->update_posting_category: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**PostingCategory**](PostingCategory.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

