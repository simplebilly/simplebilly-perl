# WWW::OpenAPIClient::Object::ApiResponseGdprExportData

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ApiResponseGdprExportData;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activity_log** | [**ARRAY[GdprActivity]**](GdprActivity.md) |  | 
**api_keys** | [**ARRAY[GdprApiKey]**](GdprApiKey.md) | Key identifiers and names only — never a usable credential. | 
**billing** | [**ARRAY[GdprBillingInfo]**](GdprBillingInfo.md) |  | 
**exported_at** | **DATE_TIME** |  | 
**generated_by_ai** | **boolean** | Honesty field: this document is a plain data dump, never AI-generated. | 
**notifications** | [**ARRAY[GdprNotification]**](GdprNotification.md) |  | 
**refresh_tokens** | [**ARRAY[GdprRefreshToken]**](GdprRefreshToken.md) | Session records: metadata only, never the token hash. | 
**tenants** | [**ARRAY[GdprTenant]**](GdprTenant.md) |  | 
**usage_events** | [**ARRAY[GdprUsageEvent]**](GdprUsageEvent.md) |  | 
**user** | [**GdprUser**](GdprUser.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


