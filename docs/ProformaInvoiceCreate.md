# WWW::OpenAPIClient::Object::ProformaInvoiceCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ProformaInvoiceCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**converted_at** | **DATE_TIME** |  | [optional] 
**converted_to_invoice_id** | **string** | Set when the proforma was converted into a real invoice. References the invoice entity. | [optional] 
**currency** | [**CurrencyCode**](CurrencyCode.md) |  | 
**customer_id** | **string** | References the customer entity. | [optional] 
**customer_snapshot** | **object** | Snapshot of the recipient at issue time (address, VAT id, …). | [optional] 
**issue_date** | **DATE** |  | 
**line_items** | **object** |  | 
**notes** | **string** |  | [optional] 
**order_number** | **string** | Reference to the order/quote this proforma belongs to. | [optional] 
**payment_due_date** | **DATE** | Optional deadline the real invoice should carry after conversion. | [optional] 
**quotation_id** | **string** | References the quotation entity. | [optional] 
**status** | [**ProformaInvoiceStatus**](ProformaInvoiceStatus.md) | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. | 
**subtotal** | **string** |  | 
**total_amount** | **string** |  | 
**total_tax** | **string** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


