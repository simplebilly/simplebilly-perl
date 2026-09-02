# WWW::OpenAPIClient::Object::Activity

## Load the model package
```perl
use WWW::OpenAPIClient::Object::Activity;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activity_type** | [**ActivityType**](ActivityType.md) | One of: call | email | meeting | task | note | 
**assigned_to** | **string** | User responsible (&#x60;employee.employee_id&#x60;). | [optional] 
**contact_id** | **string** | Contact this activity belongs to (&#x60;contact.contact_id&#x60;). References the contact entity. | [optional] 
**description** | **string** |  | [optional] 
**due_date** | **DATE** | Follow-up / Wiedervorlage date. Open activities with a due date in the past are overdue. | [optional] 
**reminder_date** | **DATE** | When to remind about the follow-up. | [optional] 
**status** | [**ActivityStatus**](ActivityStatus.md) | One of: open | done | cancelled | 
**subject** | **string** | Short subject line. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


