# WWW::OpenAPIClient::Object::SubmitResultDto

## Load the model package
```perl
use WWW::OpenAPIClient::Object::SubmitResultDto;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**answers** | **ARRAY[int]** | Selected answer indices (required for scored builtin trainings). | 
**assignment_id** | **string** |  | [optional] 
**score** | **int** | Score 0–100. Only trusted for plugin trainings without server-side scoring; builtin trainings are always re-scored from &#x60;answers&#x60;. | 
**training_code** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


