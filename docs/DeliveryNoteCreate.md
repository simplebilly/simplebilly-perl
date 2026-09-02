# WWW::OpenAPIClient::Object::DeliveryNoteCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::DeliveryNoteCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **object** |  | [optional] 
**contact_id** | **string** | References the contact entity. | [optional] 
**contact_name** | **string** |  | [optional] 
**currency** | **string** |  | 
**delivery_date** | **DATE** |  | [optional] 
**delivery_note_number** | **string** |  | [optional] 
**files** | **object** |  | [optional] 
**introduction** | **string** |  | [optional] 
**line_items** | **object** |  | [optional] 
**preceding_sales_voucher_id** | **string** | References the preceding sales voucher entity. | [optional] 
**preceding_sales_voucher_type** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] 
**remark** | **string** |  | [optional] 
**shipping_date** | **DATE** |  | [optional] 
**shipping_method** | **string** |  | [optional] 
**title** | **string** |  | [optional] 
**voucher_date** | **DATE** |  | 
**voucher_status** | [**VoucherStatus**](VoucherStatus.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


