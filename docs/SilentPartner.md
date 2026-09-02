# WWW::OpenAPIClient::Object::SilentPartner

## Load the model package
```perl
use WWW::OpenAPIClient::Object::SilentPartner;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contract_date** | **DATE** | Datum des Vertragsabschlusses. | [optional] 
**einlage** | **string** | Einlage (§ 230 HGB). | [optional] 
**gewinnquote_pct** | **string** | Gewinnbeteiligungsquote in Prozent (§ 231 HGB). | [optional] 
**gewinnvortrag** | **string** | Nicht erhobene Gewinne (§ 232 Abs. 3 HGB). | [optional] 
**instrument_type** | [**InstrumentType**](InstrumentType.md) | Instrument: \&quot;typisch\&quot; | \&quot;atypisch\&quot; | \&quot;partiarisches_darlehen\&quot; | \&quot;genussrecht\&quot;. | 
**kest_pflichtig** | **boolean** | 25 % Kapitalertragsteuer einbehalten (§ 43 Abs. 1 Nr. 3 EStG; typisch + partiarisches Darlehen). | [optional] 
**name** | **string** | Name des stillen Gesellschafters. | [optional] 
**notes** | **string** | Freitext-Notizen. | [optional] 
**verlust_verrechnungskonto** | **string** | Kumulierte Verluste gegen die Einlage (§ 232 Abs. 2 HGB, ≤ Einlage). | [optional] 
**verlustbeteiligung** | **boolean** | Verlustbeteiligung (§ 231 Abs. 2 HGB; kann ausgeschlossen werden). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


