# WWW::OpenAPIClient::DeclarationApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DeclarationApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_declaration**](DeclarationApi.md#create_declaration) | **POST** /api/v1/declarations | 
[**declaration_restore**](DeclarationApi.md#declaration_restore) | **POST** /api/v1/declarations/{id}/restore | 
[**delete_declaration**](DeclarationApi.md#delete_declaration) | **DELETE** /api/v1/declarations/{id} | 
[**get_declaration**](DeclarationApi.md#get_declaration) | **GET** /api/v1/declarations/{id} | 
[**get_declarations**](DeclarationApi.md#get_declarations) | **GET** /api/v1/declarations/ | 
[**update_declaration**](DeclarationApi.md#update_declaration) | **PUT** /api/v1/declarations/{id} | 


# **create_declaration**
> Declaration create_declaration(declaration_create => $declaration_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeclarationApi;
my $api_instance = WWW::OpenAPIClient::DeclarationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $declaration_create = WWW::OpenAPIClient::Object::DeclarationCreate->new(); # DeclarationCreate | 

eval {
    my $result = $api_instance->create_declaration(declaration_create => $declaration_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeclarationApi->create_declaration: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **declaration_create** | [**DeclarationCreate**](DeclarationCreate.md)|  | 

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **declaration_restore**
> Declaration declaration_restore(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeclarationApi;
my $api_instance = WWW::OpenAPIClient::DeclarationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->declaration_restore(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeclarationApi->declaration_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_declaration**
> delete_declaration(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeclarationApi;
my $api_instance = WWW::OpenAPIClient::DeclarationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_declaration(id => $id);
};
if ($@) {
    warn "Exception when calling DeclarationApi->delete_declaration: $@\n";
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

# **get_declaration**
> Declaration get_declaration(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeclarationApi;
my $api_instance = WWW::OpenAPIClient::DeclarationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_declaration(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeclarationApi->get_declaration: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_declarations**
> ARRAY[Declaration] get_declarations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeclarationApi;
my $api_instance = WWW::OpenAPIClient::DeclarationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_declarations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeclarationApi->get_declarations: $@\n";
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

[**ARRAY[Declaration]**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_declaration**
> Declaration update_declaration(id => $id, declaration_update => $declaration_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeclarationApi;
my $api_instance = WWW::OpenAPIClient::DeclarationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $declaration_update = WWW::OpenAPIClient::Object::DeclarationUpdate->new(); # DeclarationUpdate | 

eval {
    my $result = $api_instance->update_declaration(id => $id, declaration_update => $declaration_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeclarationApi->update_declaration: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **declaration_update** | [**DeclarationUpdate**](DeclarationUpdate.md)|  | 

### Return type

[**Declaration**](Declaration.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

