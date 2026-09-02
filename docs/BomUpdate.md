# WWW::OpenAPIClient::Object::BomUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::BomUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**components** | **object** | JSON array of &#x60;{product_id, name, quantity, unit, scrap_rate}&#x60;. | [optional] 
**description** | **string** |  | [optional] 
**name** | **string** |  | [optional] 
**output_quantity** | **int** | Output quantity per production run (defaults to 1). | [optional] 
**product_id** | **string** | The finished product this BOM produces. References the product entity. | [optional] 
**status** | [**BomStatus**](BomStatus.md) | One of: draft | active | archived | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


