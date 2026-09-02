# WWW::OpenAPIClient::ShareholderApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ShareholderApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_shareholder**](ShareholderApi.md#create_shareholder) | **POST** /api/v1/shareholders | 
[**delete_shareholder**](ShareholderApi.md#delete_shareholder) | **DELETE** /api/v1/shareholders/{id} | 
[**get_shareholder**](ShareholderApi.md#get_shareholder) | **GET** /api/v1/shareholders/{id} | 
[**get_shareholders**](ShareholderApi.md#get_shareholders) | **GET** /api/v1/shareholders/ | 
[**update_shareholder**](ShareholderApi.md#update_shareholder) | **PUT** /api/v1/shareholders/{id} | 


# **create_shareholder**
> Shareholder create_shareholder(shareholder_create => $shareholder_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShareholderApi;
my $api_instance = WWW::OpenAPIClient::ShareholderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shareholder_create = WWW::OpenAPIClient::Object::ShareholderCreate->new(); # ShareholderCreate | 

eval {
    my $result = $api_instance->create_shareholder(shareholder_create => $shareholder_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShareholderApi->create_shareholder: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shareholder_create** | [**ShareholderCreate**](ShareholderCreate.md)|  | 

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_shareholder**
> delete_shareholder(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShareholderApi;
my $api_instance = WWW::OpenAPIClient::ShareholderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_shareholder(id => $id);
};
if ($@) {
    warn "Exception when calling ShareholderApi->delete_shareholder: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_shareholder**
> Shareholder get_shareholder(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShareholderApi;
my $api_instance = WWW::OpenAPIClient::ShareholderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_shareholder(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShareholderApi->get_shareholder: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_shareholders**
> ARRAY[Shareholder] get_shareholders(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShareholderApi;
my $api_instance = WWW::OpenAPIClient::ShareholderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_shareholders(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShareholderApi->get_shareholders: $@\n";
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

[**ARRAY[Shareholder]**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_shareholder**
> Shareholder update_shareholder(id => $id, shareholder_update => $shareholder_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShareholderApi;
my $api_instance = WWW::OpenAPIClient::ShareholderApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $shareholder_update = WWW::OpenAPIClient::Object::ShareholderUpdate->new(); # ShareholderUpdate | 

eval {
    my $result = $api_instance->update_shareholder(id => $id, shareholder_update => $shareholder_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShareholderApi->update_shareholder: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **shareholder_update** | [**ShareholderUpdate**](ShareholderUpdate.md)|  | 

### Return type

[**Shareholder**](Shareholder.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

