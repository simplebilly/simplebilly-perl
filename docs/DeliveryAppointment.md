# WWW::OpenAPIClient::Object::DeliveryAppointment

## Load the model package
```perl
use WWW::OpenAPIClient::Object::DeliveryAppointment;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **string** |  | 
**notes** | **string** |  | [optional] 
**phone** | **string** |  | [optional] 
**requested_date** | **DATE** |  | 
**status** | [**DeliveryAppointmentStatus**](DeliveryAppointmentStatus.md) | One of: requested | confirmed | arrived | cancelled | completed | 
**supplier_name** | **string** |  | 
**time_slot** | **string** | e.g. \&quot;08:00-10:00\&quot; | [optional] 
**warehouse_id** | **string** | References the warehouse entity. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


