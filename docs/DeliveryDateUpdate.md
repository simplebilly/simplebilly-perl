# WWW::OpenAPIClient::Object::DeliveryDateUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::DeliveryDateUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | **string** | References the customer entity. | [optional] 
**fulfilled_date** | **DATE** | Date actually delivered (set on fulfillment). | [optional] 
**note** | **string** |  | [optional] 
**order_number** | **string** | Sales order number (&#x60;order.order_number&#x60;). | [optional] 
**original_date** | **DATE** | Original date promised before rescheduling. | [optional] 
**product_id** | **string** | Product line item this date applies to, if per-item. References the product entity. | [optional] 
**promised_date** | **DATE** | Date promised to the customer. | [optional] 
**status** | [**DeliveryDateStatus**](DeliveryDateStatus.md) | One of: promised | confirmed | rescheduled | fulfilled | late | cancelled | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


