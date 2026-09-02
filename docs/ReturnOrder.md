# WWW::OpenAPIClient::Object::ReturnOrder

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ReturnOrder;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_contact_id** | **string** | References the contact entity. | [optional] 
**customer_name** | **string** |  | [optional] 
**line_items** | **object** | JSON array of &#x60;{product_id, name, quantity, condition, restock, batch_number?}&#x60;. | [optional] 
**notes** | **string** |  | [optional] 
**order_id** | **string** | References the order entity. | [optional] 
**order_number** | **string** |  | [optional] 
**return_number** | **string** |  | 
**return_reason** | **string** |  | [optional] 
**status** | [**ReturnOrderStatus**](ReturnOrderStatus.md) | One of: requested | received | inspected | restocked | closed | 
**warehouse_id** | **string** | Warehouse into which restockable items are returned. References the warehouse entity. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


