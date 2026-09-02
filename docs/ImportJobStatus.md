# WWW::OpenAPIClient::Object::ImportJobStatus

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ImportJobStatus;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **string** | Set only when the job failed. | [optional] 
**job_id** | **string** |  | 
**processed** | **int** |  | 
**progress** | **int** | 0–100 | 
**provider** | **string** | Which competitor the import came from (lexoffice | billbee); the frontend uses it to label the job. Absent for legacy jobs. | [optional] 
**stage** | **string** | queued | fetching | downloading | importing | done | 
**status** | **string** | pending | running | done | failed | 
**total** | **int** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


