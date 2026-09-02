# WWW::OpenAPIClient::Object::WebhookSubscription

## Load the model package
```perl
use WWW::OpenAPIClient::Object::WebhookSubscription;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_type** | **string** | Event type to react to (e.g. \&quot;order.created\&quot;); \&quot;*\&quot; &#x3D; all events. | 
**is_active** | **boolean** |  | [optional] 
**name** | **string** | Human label (e.g. \&quot;Warehouse app\&quot;). | 
**secret** | **string** | Shared secret for HMAC-SHA256 signature, sent as X-Signature. | 
**url** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


