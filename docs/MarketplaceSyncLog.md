# WWW::OpenAPIClient::Object::MarketplaceSyncLog

## Load the model package
```perl
use WWW::OpenAPIClient::Object::MarketplaceSyncLog;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**completed_at** | **DATE_TIME** |  | [optional] 
**connection_id** | **string** | References the marketplace connection entity. | 
**error_message** | **string** |  | [optional] 
**items_failed** | **int** |  | 
**items_synced** | **int** |  | 
**platform** | **string** |  | 
**started_at** | **DATE_TIME** |  | 
**status** | [**SyncLogStatus**](SyncLogStatus.md) |  | 
**sync_type** | [**SyncType**](SyncType.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


