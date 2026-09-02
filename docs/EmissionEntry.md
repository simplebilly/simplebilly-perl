# WWW::OpenAPIClient::Object::EmissionEntry

## Load the model package
```perl
use WWW::OpenAPIClient::Object::EmissionEntry;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activity_value** | **string** | Activity amount in &#x60;unit&#x60; (kWh, l, km, t, tkm, EUR). | 
**category_id** | **string** | GHG-Protocol category key, e.g. \&quot;purchased_goods\&quot;, \&quot;business_travel\&quot;. | 
**description** | **string** |  | 
**ef_source** | **string** | Emission-factor source, e.g. \&quot;UBA-2024\&quot;, \&quot;DEFRA-2024\&quot;. | 
**ef_version** | **string** |  | 
**method** | [**EmissionMethod**](EmissionMethod.md) | \&quot;activity\&quot; | \&quot;spend\&quot; | \&quot;supplier\&quot;. | 
**scope** | [**GhgScope**](GhgScope.md) | GHG scope: \&quot;1\&quot; | \&quot;2\&quot; | \&quot;3\&quot;. | 
**tco2e** | **string** | Computed server-side: activity * factor / 1000, rounded to 4 dp. | 
**unit** | **string** | Unit of the activity value. | 
**updated_at** | **DATE_TIME** |  | [optional] 
**year** | **int** | Reporting year. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


