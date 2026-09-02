# WWW::OpenAPIClient::Object::ShippingRuleCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ShippingRuleCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**carrier** | **string** | Provider that auto-filled this rule (e.g. \&quot;ups\&quot;), if any. | [optional] 
**country** | [**CountryCode**](CountryCode.md) | None &#x3D; applies to all countries. | [optional] 
**delivery_time** | **string** | Delivery time text, e.g. \&quot;1-3\&quot;. | [optional] 
**is_active** | **boolean** |  | [optional] 
**max_weight_kg** | **double** |  | [optional] 
**min_weight_kg** | **double** |  | [optional] 
**name** | **string** | Delivery-method label, e.g. \&quot;Standardversand\&quot;. | 
**notes** | **string** |  | [optional] 
**price** | **string** | Shipping cost in the shop&#39;s currency. | 
**priority** | **int** | Lower wins when multiple rules match. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


