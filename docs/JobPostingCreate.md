# WWW::OpenAPIClient::Object::JobPostingCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::JobPostingCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional] 
**department** | **string** |  | [optional] 
**description** | **string** | What the job is; markdown/HTML. | 
**employment_type** | [**EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional] 
**location** | **string** |  | [optional] 
**remote** | **boolean** |  | 
**required_skills** | **object** | List of required skill names (JSON array of strings). | 
**requirements** | **string** | Structured profile of the required candidate (skills, experience). | [optional] 
**salary_max** | **int** |  | [optional] 
**salary_min** | **int** |  | [optional] 
**status** | [**JobPostingStatus**](JobPostingStatus.md) | draft | published | closed | 
**title** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


