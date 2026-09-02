# WWW::OpenAPIClient::Object::Shipment

## Load the model package
```perl
use WWW::OpenAPIClient::Object::Shipment;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delivered_at** | **DATE_TIME** |  | [optional] 
**label_url** | **string** |  | [optional] 
**line_items_shipment** | **object** |  | [optional] 
**order_id** | **string** | References the order entity. | 
**recipient_address** | **object** |  | [optional] 
**shipment_date** | **DATE** |  | 
**shipping_carrier** | **string** |  | 
**shipping_cost** | **string** |  | [optional] 
**shipping_method** | **string** |  | [optional] 
**signed_by** | **string** |  | [optional] 
**status** | **string** |  | 
**tracking_events** | **object** | Latest carrier tracking events (from the live tracking API). | [optional] 
**tracking_number** | **string** |  | [optional] 
**tracking_url** | **string** |  | [optional] 
**weight_kg** | **double** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


