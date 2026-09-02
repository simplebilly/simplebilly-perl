# WWW::OpenAPIClient::Object::Invoice

## Load the model package
```perl
use WWW::OpenAPIClient::Object::Invoice;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **object** |  | [optional] 
**billing_period_end** | **DATE** |  | [optional] 
**billing_period_start** | **DATE** |  | [optional] 
**cancellation_date** | **DATE** |  | [optional] 
**cancellation_invoice_id** | **string** | References the invoice entity. | [optional] 
**cancellation_reason** | **string** |  | [optional] 
**contract_id** | **string** | References the contract entity. | [optional] 
**currency** | [**CurrencyCode**](CurrencyCode.md) |  | 
**customer_id** | **string** | References the customer entity. | [optional] 
**discount_amount** | **string** |  | [optional] 
**discount_days** | **int** |  | [optional] 
**discount_percentage** | **string** |  | [optional] 
**document_type** | [**DocumentType**](DocumentType.md) |  | [optional] 
**dunning_level** | **int** |  | [optional] 
**input_vat_amount** | **string** |  | [optional] 
**input_vat_deductible** | **boolean** |  | [optional] 
**input_vat_percentage** | **string** |  | [optional] 
**introduction_text** | **string** |  | [optional] 
**invoice_type** | [**InvoiceType**](InvoiceType.md) |  | 
**is_cancelled** | **boolean** |  | [optional] 
**is_draft** | **boolean** |  | [optional] 
**is_eu_acquisition** | **boolean** |  | [optional] 
**is_eu_delivery** | **boolean** |  | [optional] 
**is_intra_community_acquisition** | **boolean** |  | [optional] 
**is_reverse_charge** | **boolean** |  | [optional] 
**issue_date** | **DATE** |  | 
**ledger_account** | **string** |  | [optional] 
**line_items** | **object** |  | 
**margin25a** | **boolean** |  | [optional] 
**margin25a_gross** | **string** |  | [optional] 
**margin25a_purchase_price** | **string** |  | [optional] 
**notes** | **string** |  | [optional] 
**order_number** | **string** |  | [optional] 
**original_pdf_path** | **string** |  | [optional] 
**paid_amount** | **string** |  | [optional] 
**payment_due_date** | **DATE** |  | [optional] 
**payment_status** | [**PaymentStatus**](PaymentStatus.md) |  | [optional] 
**payment_terms_text** | **string** |  | [optional] 
**preceding_sales_voucher_id** | **string** | References the preceding sales voucher entity. | [optional] 
**preceding_sales_voucher_type** | [**PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional] 
**receipt_confirmation_available** | **boolean** |  | [optional] 
**related_invoice_id** | **string** | References the invoice entity. | [optional] 
**relationship_type** | **string** |  | [optional] 
**sender_snapshot** | **object** |  | [optional] 
**sent_at** | **DATE_TIME** |  | [optional] 
**service_period_end** | **DATE** |  | [optional] 
**service_period_start** | **DATE** |  | [optional] 
**status** | [**InvoiceStatus**](InvoiceStatus.md) |  | 
**subtotal** | **string** |  | 
**supplier_id** | **string** | References the supplier entity. | [optional] 
**tax_exemption_reason** | **string** |  | [optional] 
**total_amount** | **string** |  | 
**total_tax** | **string** |  | 
**vat_country** | [**CountryCode**](CountryCode.md) |  | [optional] 
**vat_special_case** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


