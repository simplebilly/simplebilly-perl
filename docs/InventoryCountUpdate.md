# WWW::OpenAPIClient::Object::InventoryCountUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::InventoryCountUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count_date** | **DATE** |  | [optional] 
**count_number** | **string** |  | [optional] 
**line_items** | **object** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. | [optional] 
**notes** | **string** |  | [optional] 
**status** | [**InventoryCountStatus**](InventoryCountStatus.md) | One of: draft | counting | reviewed | posted | [optional] 
**warehouse_id** | **string** | References the warehouse entity. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


