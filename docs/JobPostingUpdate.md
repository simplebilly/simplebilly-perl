# WWW::OpenAPIClient::Object::JobPostingUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::JobPostingUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional] 
**department** | **string** |  | [optional] 
**description** | **string** | What the job is; markdown/HTML. | [optional] 
**employment_type** | [**EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional] 
**location** | **string** |  | [optional] 
**remote** | **boolean** |  | [optional] 
**required_skills** | **object** | List of required skill names (JSON array of strings). | [optional] 
**requirements** | **string** | Structured profile of the required candidate (skills, experience). | [optional] 
**salary_max** | **int** |  | [optional] 
**salary_min** | **int** |  | [optional] 
**status** | [**JobPostingStatus**](JobPostingStatus.md) | draft | published | closed | [optional] 
**title** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


