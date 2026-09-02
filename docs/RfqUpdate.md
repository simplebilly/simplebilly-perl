# WWW::OpenAPIClient::Object::RfqUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::RfqUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional] 
**line_items** | **object** | JSON array of &#x60;{product_id, name, sku, quantity, requested_unit_price?, quoted_unit_price?}&#x60;. | [optional] 
**notes** | **string** |  | [optional] 
**requested_date** | **DATE** |  | [optional] 
**response_date** | **DATE** |  | [optional] 
**rfq_number** | **string** |  | [optional] 
**status** | [**RfqStatus**](RfqStatus.md) | One of: draft | sent | offer_received | rejected | converted | [optional] 
**supplier_contact_id** | **string** | References the supplier entity. | [optional] 
**supplier_name** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


