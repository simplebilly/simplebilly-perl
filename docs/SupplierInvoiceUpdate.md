# WWW::OpenAPIClient::Object::SupplierInvoiceUpdate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::SupplierInvoiceUpdate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional] 
**goods_receipt_id** | **string** | References the goods receipt entity. | [optional] 
**invoice_date** | **DATE** |  | [optional] 
**invoice_number** | **string** |  | [optional] 
**line_items** | **object** | JSON array of &#x60;{product_id, name, quantity, unitPriceNet, taxRate}&#x60;. | [optional] 
**notes** | **string** |  | [optional] 
**purchase_order_id** | **string** | References the purchase order entity. | [optional] 
**status** | [**SupplierInvoiceStatus**](SupplierInvoiceStatus.md) | One of: draft | matched | has_variances | posted | cancelled | [optional] 
**supplier_contact_id** | **string** | References the supplier entity. | [optional] 
**supplier_name** | **string** |  | [optional] 
**total_gross_amount** | **string** |  | [optional] 
**total_net_amount** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


