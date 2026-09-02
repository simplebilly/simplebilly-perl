# WWW::OpenAPIClient::Object::ComplianceTrainingUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ComplianceTrainingUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**assignable** | **boolean** | Whether HR can assign this training as required for employees. | [optional] 
**code** | **string** | Stable code used by plugins and frontend players (e.g. \&quot;data_privacy\&quot;). | [optional] 
**description** | **string** |  | [optional] 
**pass_score** | **int** | Minimum score (0–100) required to pass. | [optional] 
**plugin_platform** | **string** | Marketplace plugin platform id when source &#x3D; Plugin. | [optional] 
**source** | [**TrainingSource**](TrainingSource.md) |  | [optional] 
**title** | **string** |  | [optional] 
**validity_months** | **int** | Certificate validity in months; null &#x3D; no expiry. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


