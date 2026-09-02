# WWW::OpenAPIClient::Object::KonzernStatus

## Load the model package
```perl
use WWW::OpenAPIClient::Object::KonzernStatus;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**groessenbefreit** | **boolean** |  | 
**kapitalmarktorientiert** | **boolean** |  | 
**konzernabschlusspflicht** | **boolean** |  | 
**missing_group_figures** | **boolean** | Keine group_figures-Zeile für das Jahr vorhanden → keine Größenbefreiung. | 
**mutterunternehmen** | **boolean** | Mutterunternehmen: mindestens eine beherrschte Beteiligung (§ 290 Abs. 1 HGB). | 
**parent_name** | **string** | Mutterunternehmen für die Zwischenholding-Befreiung (§ 291 HGB). | [optional] 
**parent_situs** | **string** |  | [optional] 
**participations** | [**ARRAY[KonzernBeteiligung]**](KonzernBeteiligung.md) |  | 
**thresholds** | [**KonzernThresholds**](KonzernThresholds.md) |  | 
**year** | **int** |  | 
**zwischenholding_befreit** | **boolean** |  | 
**zwischenholding_hinweis** | **string** | Hinweis zu den § 291-Voraussetzungen (EU/EWR-Sitz, geprüfter Konzernabschluss). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


