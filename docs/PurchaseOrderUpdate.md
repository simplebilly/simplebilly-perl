# WWW::OpenAPIClient::Object::PurchaseOrderUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::PurchaseOrderUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional] 
**delivery_address** | **object** |  | [optional] 
**expected_delivery_date** | **DATE** |  | [optional] 
**line_items** | **object** | JSON array of &#x60;{product_id, name, quantity, unit_price_net, tax_rate, delivery_date}&#x60;. | [optional] 
**notes** | **string** |  | [optional] 
**order_date** | **DATE** |  | [optional] 
**po_number** | **string** |  | [optional] 
**status** | [**PurchaseOrderStatus**](PurchaseOrderStatus.md) | One of: draft | ordered | partially_received | received | cancelled | [optional] 
**supplier_contact_id** | **string** | References the supplier entity. | [optional] 
**supplier_name** | **string** |  | [optional] 
**total_gross_amount** | **string** |  | [optional] 
**total_net_amount** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


