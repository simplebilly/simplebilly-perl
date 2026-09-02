# WWW::OpenAPIClient::Object::ServiceAssignment

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ServiceAssignment;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**employee_id** | **string** | References the employees entity. | [optional] 
**job_id** | **string** | References the service_jobs entity. | [optional] 
**notes** | **string** |  | [optional] 
**scheduled_date** | **DATE** | Work day the assignment is scheduled for. | [optional] 
**scheduled_end** | **string** | Planned end time of the assignment. | [optional] 
**scheduled_start** | **string** | Planned start time of the assignment. | [optional] 
**status** | [**ServiceAssignmentStatus**](ServiceAssignmentStatus.md) | Assignment lifecycle status: \&quot;planned\&quot;, \&quot;confirmed\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot; or \&quot;cancelled\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


