# WWW::OpenAPIClient::Object::GoodsReceipt

## Load the model package
```perl
use WWW::OpenAPIClient::Object::GoodsReceipt;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**gr_number** | **string** |  | 
**line_items** | **object** | JSON array of &#x60;{product_id, name, quantity, batch_number?, expiry_date?, bin_location?}&#x60;. | 
**notes** | **string** |  | [optional] 
**purchase_order_id** | **string** | References the purchase order entity. | [optional] 
**receipt_date** | **DATE** |  | 
**supplier_contact_id** | **string** | References the supplier entity. | [optional] 
**supplier_name** | **string** |  | [optional] 
**warehouse_id** | **string** | References the warehouse entity. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


