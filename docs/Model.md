# WWW::OpenAPIClient::Object::Model

## Load the model package
```perl
use WWW::OpenAPIClient::Object::Model;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backup_codes** | **ARRAY[string]** |  | 
**created_at** | **DATE_TIME** |  | 
**deleted_at** | **DATE_TIME** |  | [optional] 
**email** | **string** |  | 
**email_verified** | **boolean** |  | 
**id** | **string** |  | 
**is_active** | **boolean** |  | 
**is_totp_enabled** | **boolean** |  | 
**last_login** | **DATE_TIME** |  | [optional] 
**name** | **string** |  | 
**oauth_id** | **string** |  | [optional] 
**oauth_provider** | **string** |  | [optional] 
**password_changed_at** | **DATE_TIME** | Set on password change; auth/refresh tokens issued before this timestamp are rejected by the auth middleware. | [optional] 
**password_hash** | **string** |  | 
**picture** | **string** |  | [optional] 
**privacy_accepted_at** | **DATE_TIME** | When the user accepted the data privacy policy (GDPR consent record). | [optional] 
**totp_secret** | **string** |  | [optional] 
**updated_at** | **DATE_TIME** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


