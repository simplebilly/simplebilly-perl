# WWW::OpenAPIClient::Object::InventoryCount

## Load the model package
```perl
use WWW::OpenAPIClient::Object::InventoryCount;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count_date** | **DATE** |  | 
**count_number** | **string** |  | 
**line_items** | **object** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. | 
**notes** | **string** |  | [optional] 
**status** | [**InventoryCountStatus**](InventoryCountStatus.md) | One of: draft | counting | reviewed | posted | 
**warehouse_id** | **string** | References the warehouse entity. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


