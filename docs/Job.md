# WWW::OpenAPIClient::Object::Job

## Load the model package
```perl
use WWW::OpenAPIClient::Object::Job;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **int** |  | [optional] 
**job_type** | **string** | Discriminator the worker dispatches on (e.g. \&quot;webhook.deliver\&quot;). | 
**max_attempts** | **int** |  | 
**payload** | **object** |  | [optional] 
**run_at** | **DATE_TIME** | Earliest execution time; None &#x3D; run now. | [optional] 
**status** | [**JobStatus**](JobStatus.md) | pending | running | done | failed | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


