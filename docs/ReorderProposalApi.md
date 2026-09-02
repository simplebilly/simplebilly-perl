# WWW::OpenAPIClient::ReorderProposalApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ReorderProposalApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**apply_reorder_proposal**](ReorderProposalApi.md#apply_reorder_proposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order.
[**get_reorder_proposal**](ReorderProposalApi.md#get_reorder_proposal) | **GET** /api/v1/reorder-proposals | 


# **apply_reorder_proposal**
> object apply_reorder_proposal(configured_only => $configured_only, warehouse_id => $warehouse_id)

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReorderProposalApi;
my $api_instance = WWW::OpenAPIClient::ReorderProposalApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $configured_only = null; # boolean | Only include products with a reorder point configured (`min_stock`).
my $warehouse_id = "warehouse_id_example"; # string | Limit to a single warehouse id.

eval {
    my $result = $api_instance->apply_reorder_proposal(configured_only => $configured_only, warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReorderProposalApi->apply_reorder_proposal: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **configured_only** | **boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] 
 **warehouse_id** | **string**| Limit to a single warehouse id. | [optional] 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_reorder_proposal**
> ReorderProposalResponse get_reorder_proposal(configured_only => $configured_only, warehouse_id => $warehouse_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ReorderProposalApi;
my $api_instance = WWW::OpenAPIClient::ReorderProposalApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $configured_only = null; # boolean | Only include products with a reorder point configured (`min_stock`).
my $warehouse_id = "warehouse_id_example"; # string | Limit to a single warehouse id.

eval {
    my $result = $api_instance->get_reorder_proposal(configured_only => $configured_only, warehouse_id => $warehouse_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ReorderProposalApi->get_reorder_proposal: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **configured_only** | **boolean**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] 
 **warehouse_id** | **string**| Limit to a single warehouse id. | [optional] 

### Return type

[**ReorderProposalResponse**](ReorderProposalResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

