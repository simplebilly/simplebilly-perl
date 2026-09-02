# WWW::OpenAPIClient::Object::CustomerCommunicationCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::CustomerCommunicationCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **string** | The message body, call summary or note text. | [optional] 
**channel** | [**CommunicationChannel**](CommunicationChannel.md) |  | 
**contact_id** | **string** | The contact (customer/supplier) this communication belongs to. References the contact entity. | 
**counterparty** | **string** | Email/phone of the counterparty, if applicable. | [optional] 
**direction** | [**CommunicationDirection**](CommunicationDirection.md) |  | 
**occurred_at** | **DATE_TIME** | When the communication happened (defaults to now on create). | [optional] 
**subject** | **string** |  | [optional] 
**tags** | **object** | Free-form tags, e.g. &#x60;[\&quot;follow-up-required\&quot;]&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


