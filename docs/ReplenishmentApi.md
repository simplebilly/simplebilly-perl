# WWW::OpenAPIClient::ReplenishmentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ReplenishmentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apply_replenishments**](ReplenishmentApi.md#apply_replenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
[**get_replenishments**](ReplenishmentApi.md#get_replenishments) | **GET** /api/v1/replenishments | 


# **apply_replenishments**
> object apply_replenishments(target_warehouse_id => $target_warehouse_id, source_warehouse_id => $source_warehouse_id)

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReplenishmentApi;
my $api_instance = WWW::OpenAPIClient::ReplenishmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $target_warehouse_id = "target_warehouse_id_example"; # string | Warehouse to be replenished. Defaults to the tenant's default warehouse.
my $source_warehouse_id = "source_warehouse_id_example"; # string | Restrict source warehouses to this id.

eval {
    my $result = $api_instance->apply_replenishments(target_warehouse_id => $target_warehouse_id, source_warehouse_id => $source_warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReplenishmentApi->apply_replenishments: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **target_warehouse_id** | **string**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] 
 **source_warehouse_id** | **string**| Restrict source warehouses to this id. | [optional] 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_replenishments**
> ReplenishmentResponse get_replenishments(target_warehouse_id => $target_warehouse_id, source_warehouse_id => $source_warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReplenishmentApi;
my $api_instance = WWW::OpenAPIClient::ReplenishmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $target_warehouse_id = "target_warehouse_id_example"; # string | Warehouse to be replenished. Defaults to the tenant's default warehouse.
my $source_warehouse_id = "source_warehouse_id_example"; # string | Restrict source warehouses to this id.

eval {
    my $result = $api_instance->get_replenishments(target_warehouse_id => $target_warehouse_id, source_warehouse_id => $source_warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReplenishmentApi->get_replenishments: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **target_warehouse_id** | **string**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] 
 **source_warehouse_id** | **string**| Restrict source warehouses to this id. | [optional] 

### Return type

[**ReplenishmentResponse**](ReplenishmentResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

