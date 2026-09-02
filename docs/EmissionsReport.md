# WWW::OpenAPIClient::Object::EmissionsReport

## Load the model package
```perl
use WWW::OpenAPIClient::Object::EmissionsReport;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**by_category** | [**ARRAY[CategoryTotal]**](CategoryTotal.md) |  | 
**by_scope** | [**ARRAY[ScopeTotal]**](ScopeTotal.md) |  | 
**by_year** | [**ARRAY[YearTotal]**](YearTotal.md) |  | 
**data_quality** | [**DataQuality**](DataQuality.md) |  | 
**intensity_per_employee** | **double** |  | [optional] 
**intensity_per_revenue_mio** | **double** | tCO2e per million EUR net revenue. | [optional] 
**net_revenue** | **double** | Sum of paid/sent/partially-paid invoices (EUR net) in the year. | [optional] 
**spend_based_estimate_tco2e** | **double** | Spend-based estimate from bookkeeping payments (EXIOBASE factor). | [optional] 
**targets** | [**ARRAY[TargetProgress]**](TargetProgress.md) |  | 
**total_tco2e** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


