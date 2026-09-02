# WWW::OpenAPIClient::Object::ApiResponseSubscriptionOverviewData

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ApiResponseSubscriptionOverviewData;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_period_end** | **DATE_TIME** |  | [optional] 
**features** | [**PlanFeatures**](PlanFeatures.md) |  | 
**is_trialing** | **boolean** |  | 
**limits** | [**PlanLimits**](PlanLimits.md) |  | 
**manage_url** | **string** |  | [optional] 
**plan** | **string** | Resolved plan id (free/starter/business/enterprise, or a custom override id). | 
**plan_name** | **string** |  | 
**price_eur** | **double** | Monthly price in EUR; &#x60;-1.0&#x60; &#x3D; custom pricing (enterprise). | 
**quantity** | **int** |  | [optional] 
**status** | **string** |  | [optional] 
**subscription_id** | **string** |  | [optional] 
**trial_ends_at** | **DATE_TIME** |  | [optional] 
**usage** | [**UsageSnapshot**](UsageSnapshot.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


