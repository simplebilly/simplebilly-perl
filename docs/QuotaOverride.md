# WWW::OpenAPIClient::Object::QuotaOverride

## Load the model package
```perl
use WWW::OpenAPIClient::Object::QuotaOverride;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**features** | [**QuotaOverrideFeatures**](QuotaOverrideFeatures.md) |  | [optional] 
**max_connectors** | **int** |  | [optional] 
**max_invoices_per_month** | **int** |  | [optional] 
**max_users** | **int** |  | [optional] 
**metered** | **HASH[string,int]** |  | [optional] 
**plan** | **string** | Custom plan id; unknown ids resolve to enterprise limits. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


