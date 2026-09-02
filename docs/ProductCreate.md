# WWW::OpenAPIClient::Object::ProductCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ProductCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**availability** | **string** |  | [optional] 
**barcode** | **string** |  | [optional] 
**brand** | **string** |  | [optional] 
**category_id** | **string** |  | [optional] 
**condition** | **string** |  | [optional] 
**default_ledger_account** | **string** |  | [optional] 
**default_price** | **string** |  | [optional] 
**default_price_formula_id** | **string** | References the price formula entity. | [optional] 
**default_tax_rate** | **string** |  | [optional] 
**description** | **string** |  | [optional] 
**gtin** | **string** |  | [optional] 
**height** | **string** |  | [optional] 
**image_link** | **string** |  | [optional] 
**images** | **object** |  | [optional] 
**is_taxable** | **boolean** |  | [optional] 
**length** | **string** |  | [optional] 
**link** | **string** |  | [optional] 
**max_stock** | **int** | Target stock level used by reorder proposals. | [optional] 
**min_stock** | **int** | Reorder point — when stock falls below this, a reorder is suggested. | [optional] 
**mpn** | **string** |  | [optional] 
**name** | **string** |  | 
**package_height** | **string** |  | [optional] 
**package_length** | **string** |  | [optional] 
**package_weight_unit** | **string** |  | [optional] 
**package_weight_value** | **string** |  | [optional] 
**package_width** | **string** |  | [optional] 
**product_code** | **string** |  | 
**product_type** | **string** |  | [optional] 
**purchase_price** | **string** |  | [optional] 
**reorder_quantity** | **int** | Suggested purchase quantity when a reorder proposal is created. | [optional] 
**sale_price** | **string** |  | [optional] 
**shipping_price** | **string** |  | [optional] 
**shipping_requires_insurance** | **boolean** |  | [optional] 
**sku** | **string** |  | 
**stock_quantity** | **int** |  | [optional] 
**tags** | **object** |  | [optional] 
**tax_price** | **string** |  | [optional] 
**track_batch** | **boolean** | Whether this product requires batch (Chargennummer) tracking. | [optional] 
**track_serial** | **boolean** | Whether this product requires serial-number tracking. | [optional] 
**unit** | **object** |  | [optional] 
**weight_unit** | **string** |  | [optional] 
**weight_value** | **string** |  | [optional] 
**width** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


