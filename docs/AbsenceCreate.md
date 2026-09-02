# WWW::OpenAPIClient::Object::AbsenceCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::AbsenceCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**absence_type** | [**AbsenceType**](AbsenceType.md) | One of \&quot;vacation\&quot;, \&quot;sick\&quot;, \&quot;sabbatical\&quot;, \&quot;parental\&quot;, \&quot;other\&quot;. | [optional] 
**approved_at** | **DATE_TIME** |  | [optional] 
**approved_by** | **string** | References the user entity. | [optional] 
**employee_id** | **string** | References the employee entity. | [optional] 
**end_date** | **DATE** |  | [optional] 
**notes** | **string** |  | [optional] 
**start_date** | **DATE** |  | [optional] 
**status** | [**AbsenceStatus**](AbsenceStatus.md) | One of \&quot;pending\&quot;, \&quot;approved\&quot;, \&quot;rejected\&quot;, \&quot;cancelled\&quot;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


