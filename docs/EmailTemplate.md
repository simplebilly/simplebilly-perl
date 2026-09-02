# WWW::OpenAPIClient::Object::EmailTemplate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::EmailTemplate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **string** | E-mail body with optional placeholders. | 
**name** | **string** | Human-readable template name, e.g. \&quot;Follow-up after quote\&quot;. | 
**status** | [**EmailTemplateStatus**](EmailTemplateStatus.md) | One of: active | inactive | 
**subject** | **string** | E-mail subject line with optional placeholders. | 
**variables** | **object** | Placeholders used by this template, e.g. &#x60;[\&quot;contact.first_name\&quot;]&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


