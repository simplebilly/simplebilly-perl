# WWW::OpenAPIClient::Object::SupportTicket

## Load the model package
```perl
use WWW::OpenAPIClient::Object::SupportTicket;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assigned_to** | **string** |  | [optional] 
**channel_id** | **string** |  | [optional] 
**channel_type** | [**SupportChannelType**](SupportChannelType.md) |  | [optional] 
**closed_at** | **DATE_TIME** |  | [optional] 
**created_at** | **DATE_TIME** |  | 
**customer_email** | **string** |  | [optional] 
**customer_id** | **string** | References the customer entity. | [optional] 
**customer_name** | **string** |  | [optional] 
**external_id** | **string** |  | [optional] 
**first_message_at** | **DATE_TIME** |  | 
**last_message_at** | **DATE_TIME** |  | 
**lead_id** | **string** | References the lead entity. | [optional] 
**message_count** | **int** |  | 
**order_ref** | **string** |  | [optional] 
**priority** | [**TicketPriority**](TicketPriority.md) |  | 
**resolution** | **string** |  | [optional] 
**status** | [**SupportTicketStatus**](SupportTicketStatus.md) |  | 
**subject** | **string** |  | 
**tags** | **object** |  | 
**tenant_id** | **string** |  | 
**updated_at** | **DATE_TIME** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


