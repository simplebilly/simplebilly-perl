# WWW::OpenAPIClient::Object::PlanLimits

## Load the model package
```perl
use WWW::OpenAPIClient::Object::PlanLimits;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**max_connectors** | **int** |  | 
**max_invoices_per_month** | **int** |  | 
**max_users** | **int** |  | 
**metered** | **HASH[string,int]** |  | [optional] 
**paid_connectors** | **ARRAY[string]** | Connectors that are *not* included in this plan (require a higher tier). Empty &#x3D; all connectors included on this plan. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


