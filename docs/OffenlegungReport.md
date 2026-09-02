# WWW::OpenAPIClient::Object::OffenlegungReport

## Load the model package
```perl
use WWW::OpenAPIClient::Object::OffenlegungReport;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**deadline** | **DATE** | Fristende (Abschlussstichtag + Frist). | 
**deadline_months** | **int** | Offenlegungsfrist in Monaten (§ 325 Abs. 4 HGB). | 
**items** | [**ARRAY[OffenlegungItem]**](OffenlegungItem.md) |  | 
**kapitalmarktorientiert** | **boolean** | Annahme über die Kapitalmarktorientierung. | 
**note** | **string** |  | 
**year** | **int** | Berichtsjahr (laufendes Kalenderjahr). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


