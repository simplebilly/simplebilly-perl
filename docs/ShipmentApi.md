# WWW::OpenAPIClient::ShipmentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ShipmentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_shipment**](ShipmentApi.md#create_shipment) | **POST** /api/v1/shipments | 
[**create_shipment_from_order**](ShipmentApi.md#create_shipment_from_order) | **POST** /api/v1/orders/{order_number}/shipments | Create a real shipment for an order: calls the configured carrier&#39;s label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
[**delete_shipment**](ShipmentApi.md#delete_shipment) | **DELETE** /api/v1/shipments/{shipment_id} | 
[**get_shipment**](ShipmentApi.md#get_shipment) | **GET** /api/v1/shipments/{shipment_id} | 
[**list_shipments**](ShipmentApi.md#list_shipments) | **GET** /api/v1/shipments | 
[**track_order_public**](ShipmentApi.md#track_order_public) | **POST** /api/v1/public/track | Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
[**track_shipment_api**](ShipmentApi.md#track_shipment_api) | **GET** /api/v1/shipments/{shipment_id}/tracking | 
[**update_shipment_status**](ShipmentApi.md#update_shipment_status) | **PUT** /api/v1/shipments/{shipment_id}/status | 


# **create_shipment**
> Shipment create_shipment(shipment => $shipment)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipment = WWW::OpenAPIClient::Object::Shipment->new(); # Shipment | 

eval {
    my $result = $api_instance->create_shipment(shipment => $shipment);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShipmentApi->create_shipment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipment** | [**Shipment**](Shipment.md)|  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_shipment_from_order**
> Shipment create_shipment_from_order(order_number => $order_number, create_shipment_request => $create_shipment_request)

Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 
my $create_shipment_request = WWW::OpenAPIClient::Object::CreateShipmentRequest->new(); # CreateShipmentRequest | 

eval {
    my $result = $api_instance->create_shipment_from_order(order_number => $order_number, create_shipment_request => $create_shipment_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShipmentApi->create_shipment_from_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 
 **create_shipment_request** | [**CreateShipmentRequest**](CreateShipmentRequest.md)|  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_shipment**
> delete_shipment(shipment_id => $shipment_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipment_id = "shipment_id_example"; # string | 

eval {
    $api_instance->delete_shipment(shipment_id => $shipment_id);
};
if ($@) {
    warn "Exception when calling ShipmentApi->delete_shipment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipment_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_shipment**
> Shipment get_shipment(shipment_id => $shipment_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipment_id = "shipment_id_example"; # string | 

eval {
    my $result = $api_instance->get_shipment(shipment_id => $shipment_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShipmentApi->get_shipment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipment_id** | **string**|  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_shipments**
> ARRAY[Shipment] list_shipments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->list_shipments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShipmentApi->list_shipments: $@\n";
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

[**ARRAY[Shipment]**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **track_order_public**
> TrackOrderResponse track_order_public(track_order_request => $track_order_request)

Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $track_order_request = WWW::OpenAPIClient::Object::TrackOrderRequest->new(); # TrackOrderRequest | 

eval {
    my $result = $api_instance->track_order_public(track_order_request => $track_order_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShipmentApi->track_order_public: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **track_order_request** | [**TrackOrderRequest**](TrackOrderRequest.md)|  | 

### Return type

[**TrackOrderResponse**](TrackOrderResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **track_shipment_api**
> TrackingInfo track_shipment_api(shipment_id => $shipment_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipment_id = "shipment_id_example"; # string | 

eval {
    my $result = $api_instance->track_shipment_api(shipment_id => $shipment_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShipmentApi->track_shipment_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipment_id** | **string**|  | 

### Return type

[**TrackingInfo**](TrackingInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_shipment_status**
> Shipment update_shipment_status(shipment_id => $shipment_id, shipment_status_update => $shipment_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShipmentApi;
my $api_instance = WWW::OpenAPIClient::ShipmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $shipment_id = "shipment_id_example"; # string | 
my $shipment_status_update = WWW::OpenAPIClient::Object::ShipmentStatusUpdate->new(); # ShipmentStatusUpdate | 

eval {
    my $result = $api_instance->update_shipment_status(shipment_id => $shipment_id, shipment_status_update => $shipment_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShipmentApi->update_shipment_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **shipment_id** | **string**|  | 
 **shipment_status_update** | [**ShipmentStatusUpdate**](ShipmentStatusUpdate.md)|  | 

### Return type

[**Shipment**](Shipment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

