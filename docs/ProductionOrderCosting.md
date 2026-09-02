# WWW::OpenAPIClient::Object::ProductionOrderCosting

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ProductionOrderCosting;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cost_per_unit** | **string** | material_cost_total ÷ quantity. | 
**cost_source** | **string** | \&quot;actual\&quot; when costed from stock-movement consumption, else \&quot;planned\&quot;. | 
**lines** | [**ARRAY[CostingLine]**](CostingLine.md) |  | 
**margin_per_unit** | **string** | sale_price − cost_per_unit. | [optional] 
**margin_percent** | **string** | margin_per_unit ÷ cost_per_unit as a percentage. | [optional] 
**material_cost_total** | **string** | Total material cost for the whole order. | 
**order_number** | **string** |  | 
**production_order_id** | **string** |  | 
**quantity** | **int** |  | 
**sale_price** | **string** | Finished product&#39;s sale price per unit (used to compute margin). | [optional] 
**status** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


