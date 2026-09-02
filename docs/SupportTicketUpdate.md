# WWW::OpenAPIClient::Object::SupportTicketUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::SupportTicketUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assigned_to** | **string** |  | [optional] 
**channel_id** | **string** |  | [optional] 
**channel_type** | [**SupportChannelType**](SupportChannelType.md) |  | [optional] 
**closed_at** | **DATE_TIME** |  | [optional] 
**created_at** | **DATE_TIME** |  | [optional] 
**customer_email** | **string** |  | [optional] 
**customer_id** | **string** | References the customer entity. | [optional] 
**customer_name** | **string** |  | [optional] 
**external_id** | **string** |  | [optional] 
**first_message_at** | **DATE_TIME** |  | [optional] 
**last_message_at** | **DATE_TIME** |  | [optional] 
**lead_id** | **string** | References the lead entity. | [optional] 
**message_count** | **int** |  | [optional] 
**order_ref** | **string** |  | [optional] 
**priority** | [**TicketPriority**](TicketPriority.md) |  | [optional] 
**resolution** | **string** |  | [optional] 
**status** | [**SupportTicketStatus**](SupportTicketStatus.md) |  | [optional] 
**subject** | **string** |  | [optional] 
**tags** | **object** |  | [optional] 
**tenant_id** | **string** |  | [optional] 
**updated_at** | **DATE_TIME** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


