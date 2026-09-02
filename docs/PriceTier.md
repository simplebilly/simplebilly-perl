# WWW::OpenAPIClient::Object::PriceTier

## Load the model package
```perl
use WWW::OpenAPIClient::Object::PriceTier;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_group_id** | **string** | None &#x3D; tier applies to all customers; otherwise a customer group id. | [optional] 
**min_quantity** | **int** | Quantity from which this tier applies (inclusive). | [optional] 
**product_id** | **string** | References the product entity. | 
**unit_price** | **string** | Net unit price once &#x60;min_quantity&#x60; is reached. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


