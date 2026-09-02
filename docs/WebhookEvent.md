# WWW::OpenAPIClient::Object::WebhookEvent

## Load the model package
```perl
use WWW::OpenAPIClient::Object::WebhookEvent;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **int** |  | [optional] 
**channel** | **string** | source for inbound, target URL for outbound. | [optional] 
**direction** | [**WebhookDirection**](WebhookDirection.md) | inbound | outbound | 
**event_type** | **string** |  | 
**last_error** | **string** |  | [optional] 
**payload** | **object** |  | [optional] 
**status** | [**WebhookEventStatus**](WebhookEventStatus.md) | accepted | delivered | failed | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


