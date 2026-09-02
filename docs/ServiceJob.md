# WWW::OpenAPIClient::Object::ServiceJob

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ServiceJob;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **string** | Street + zip + city of the job location. | [optional] 
**customer_email** | **string** | Customer email for email notifications. | [optional] 
**customer_id** | **string** | References the customer entity. | [optional] 
**customer_name** | **string** | Denormalized customer name for quick display. | [optional] 
**customer_phone** | **string** | Customer phone for SMS notifications later. | [optional] 
**description** | **string** | What work needs to be done. | [optional] 
**estimated_duration_minutes** | **int** | Estimated time for the job in minutes. | [optional] 
**lat** | **double** | Latitude for map display (OpenStreetMap). | [optional] 
**lng** | **double** | Longitude for map display (OpenStreetMap). | [optional] 
**notes** | **string** |  | [optional] 
**status** | [**ServiceJobStatus**](ServiceJobStatus.md) | Dispatch status: \&quot;pending\&quot;, \&quot;assigned\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot;, \&quot;cancelled\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


