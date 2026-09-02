# WWW::OpenAPIClient::Object::ComplianceTraining

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ComplianceTraining;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assignable** | **boolean** | Whether HR can assign this training as required for employees. | [optional] 
**code** | **string** | Stable code used by plugins and frontend players (e.g. \&quot;data_privacy\&quot;). | [optional] 
**created_at** | **DATE_TIME** |  | [optional] 
**deleted_at** | **DATE_TIME** |  | [optional] 
**description** | **string** |  | [optional] 
**id** | **string** |  | [optional] 
**pass_score** | **int** | Minimum score (0–100) required to pass. | [optional] 
**plugin_platform** | **string** | Marketplace plugin platform id when source &#x3D; Plugin. | [optional] 
**source** | [**TrainingSource**](TrainingSource.md) |  | [optional] 
**tenant_id** | **string** |  | [optional] 
**title** | **string** |  | [optional] 
**updated_at** | **DATE_TIME** |  | [optional] 
**validity_months** | **int** | Certificate validity in months; null &#x3D; no expiry. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


