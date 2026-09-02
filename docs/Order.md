# WWW::OpenAPIClient::Object::Order

## Load the model package
```perl
use WWW::OpenAPIClient::Object::Order;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**audit_log** | **object** |  | [optional] 
**currency** | **string** |  | 
**customer_id** | **string** | References the customer entity. | 
**external_reference** | **string** |  | [optional] 
**invoice_address** | **object** |  | [optional] 
**items** | **object** |  | [optional] 
**language** | [**LanguageCode**](LanguageCode.md) |  | [optional] 
**order_status** | [**OrderStatus**](OrderStatus.md) |  | 
**payment_method** | [**PaymentMethod**](PaymentMethod.md) |  | 
**shipping_address** | **object** |  | [optional] 
**shipping_cost** | **string** |  | 
**shipping_method** | **string** |  | 
**shipping_weight** | **string** |  | 
**tags** | **ARRAY[string]** |  | 
**total_cost** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


