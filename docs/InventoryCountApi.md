# WWW::OpenAPIClient::InventoryCountApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::InventoryCountApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_inventory_count**](InventoryCountApi.md#create_inventory_count) | **POST** /api/v1/inventory-counts | 
[**delete_inventory_count**](InventoryCountApi.md#delete_inventory_count) | **DELETE** /api/v1/inventory-counts/{inventory_count_id} | 
[**generate_inventory_count**](InventoryCountApi.md#generate_inventory_count) | **POST** /api/v1/inventory-counts/generate | 
[**get_inventory_count**](InventoryCountApi.md#get_inventory_count) | **GET** /api/v1/inventory-counts/{inventory_count_id} | 
[**list_inventory_counts**](InventoryCountApi.md#list_inventory_counts) | **GET** /api/v1/inventory-counts/ | 
[**update_inventory_count**](InventoryCountApi.md#update_inventory_count) | **PUT** /api/v1/inventory-counts/{inventory_count_id} | 
[**update_inventory_count_status**](InventoryCountApi.md#update_inventory_count_status) | **PUT** /api/v1/inventory-counts/{inventory_count_id}/status | 


# **create_inventory_count**
> InventoryCount create_inventory_count(inventory_count => $inventory_count)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryCountApi;
my $api_instance = WWW::OpenAPIClient::InventoryCountApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $inventory_count = WWW::OpenAPIClient::Object::InventoryCount->new(); # InventoryCount | 

eval {
    my $result = $api_instance->create_inventory_count(inventory_count => $inventory_count);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryCountApi->create_inventory_count: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inventory_count** | [**InventoryCount**](InventoryCount.md)|  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_inventory_count**
> delete_inventory_count(inventory_count_id => $inventory_count_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryCountApi;
my $api_instance = WWW::OpenAPIClient::InventoryCountApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $inventory_count_id = "inventory_count_id_example"; # string | 

eval {
    $api_instance->delete_inventory_count(inventory_count_id => $inventory_count_id);
};
if ($@) {
    warn "Exception when calling InventoryCountApi->delete_inventory_count: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inventory_count_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_inventory_count**
> InventoryCount generate_inventory_count(generate_count_request => $generate_count_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryCountApi;
my $api_instance = WWW::OpenAPIClient::InventoryCountApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $generate_count_request = WWW::OpenAPIClient::Object::GenerateCountRequest->new(); # GenerateCountRequest | 

eval {
    my $result = $api_instance->generate_inventory_count(generate_count_request => $generate_count_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryCountApi->generate_inventory_count: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **generate_count_request** | [**GenerateCountRequest**](GenerateCountRequest.md)|  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_inventory_count**
> InventoryCount get_inventory_count(inventory_count_id => $inventory_count_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryCountApi;
my $api_instance = WWW::OpenAPIClient::InventoryCountApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $inventory_count_id = "inventory_count_id_example"; # string | 

eval {
    my $result = $api_instance->get_inventory_count(inventory_count_id => $inventory_count_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryCountApi->get_inventory_count: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inventory_count_id** | **string**|  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_inventory_counts**
> ARRAY[InventoryCount] list_inventory_counts(page => $page, page_size => $page_size, status => $status, warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryCountApi;
my $api_instance = WWW::OpenAPIClient::InventoryCountApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $warehouse_id = "warehouse_id_example"; # string | 

eval {
    my $result = $api_instance->list_inventory_counts(page => $page, page_size => $page_size, status => $status, warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryCountApi->list_inventory_counts: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **warehouse_id** | **string**|  | [optional] 

### Return type

[**ARRAY[InventoryCount]**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_inventory_count**
> InventoryCount update_inventory_count(inventory_count_id => $inventory_count_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryCountApi;
my $api_instance = WWW::OpenAPIClient::InventoryCountApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $inventory_count_id = "inventory_count_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_inventory_count(inventory_count_id => $inventory_count_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryCountApi->update_inventory_count: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inventory_count_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_inventory_count_status**
> InventoryCount update_inventory_count_status(inventory_count_id => $inventory_count_id, inventory_count_status_update => $inventory_count_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InventoryCountApi;
my $api_instance = WWW::OpenAPIClient::InventoryCountApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $inventory_count_id = "inventory_count_id_example"; # string | 
my $inventory_count_status_update = WWW::OpenAPIClient::Object::InventoryCountStatusUpdate->new(); # InventoryCountStatusUpdate | 

eval {
    my $result = $api_instance->update_inventory_count_status(inventory_count_id => $inventory_count_id, inventory_count_status_update => $inventory_count_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InventoryCountApi->update_inventory_count_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **inventory_count_id** | **string**|  | 
 **inventory_count_status_update** | [**InventoryCountStatusUpdate**](InventoryCountStatusUpdate.md)|  | 

### Return type

[**InventoryCount**](InventoryCount.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

