# WWW::OpenAPIClient::BomApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::BomApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_bom**](BomApi.md#create_bom) | **POST** /api/v1/boms | 
[**delete_bom**](BomApi.md#delete_bom) | **DELETE** /api/v1/boms/{bom_id} | 
[**get_bom**](BomApi.md#get_bom) | **GET** /api/v1/boms/{bom_id} | 
[**list_boms**](BomApi.md#list_boms) | **GET** /api/v1/boms/ | 
[**update_bom**](BomApi.md#update_bom) | **PUT** /api/v1/boms/{bom_id} | 


# **create_bom**
> Bom create_bom(bom_create => $bom_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BomApi;
my $api_instance = WWW::OpenAPIClient::BomApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $bom_create = WWW::OpenAPIClient::Object::BomCreate->new(); # BomCreate | 

eval {
    my $result = $api_instance->create_bom(bom_create => $bom_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BomApi->create_bom: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bom_create** | [**BomCreate**](BomCreate.md)|  | 

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_bom**
> delete_bom(bom_id => $bom_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BomApi;
my $api_instance = WWW::OpenAPIClient::BomApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $bom_id = "bom_id_example"; # string | 

eval {
    $api_instance->delete_bom(bom_id => $bom_id);
};
if ($@) {
    warn "Exception when calling BomApi->delete_bom: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bom_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_bom**
> Bom get_bom(bom_id => $bom_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BomApi;
my $api_instance = WWW::OpenAPIClient::BomApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $bom_id = "bom_id_example"; # string | 

eval {
    my $result = $api_instance->get_bom(bom_id => $bom_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BomApi->get_bom: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bom_id** | **string**|  | 

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_boms**
> ARRAY[Bom] list_boms(page => $page, page_size => $page_size, search => $search, product_id => $product_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BomApi;
my $api_instance = WWW::OpenAPIClient::BomApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $product_id = "product_id_example"; # string | Filter by finished product id.

eval {
    my $result = $api_instance->list_boms(page => $page, page_size => $page_size, search => $search, product_id => $product_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BomApi->list_boms: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **product_id** | **string**| Filter by finished product id. | [optional] 

### Return type

[**ARRAY[Bom]**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_bom**
> Bom update_bom(bom_id => $bom_id, bom_update => $bom_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BomApi;
my $api_instance = WWW::OpenAPIClient::BomApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $bom_id = "bom_id_example"; # string | 
my $bom_update = WWW::OpenAPIClient::Object::BomUpdate->new(); # BomUpdate | 

eval {
    my $result = $api_instance->update_bom(bom_id => $bom_id, bom_update => $bom_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BomApi->update_bom: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bom_id** | **string**|  | 
 **bom_update** | [**BomUpdate**](BomUpdate.md)|  | 

### Return type

[**Bom**](Bom.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

