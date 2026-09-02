# WWW::OpenAPIClient::CreateSepaDirectDebitApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::CreateSepaDirectDebitApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_sepa_direct_debit_api**](CreateSepaDirectDebitApi.md#create_sepa_direct_debit_api) | **POST** /api/v1/bookkeeping/sepa-direct-debit | 


# **create_sepa_direct_debit_api**
> SepaDirectDebitResponse create_sepa_direct_debit_api(creditor_name => $creditor_name, creditor_iban => $creditor_iban, creditor_id => $creditor_id, mandate_id => $mandate_id, mandate_date => $mandate_date, debtor_name => $debtor_name, debtor_iban => $debtor_iban, amount => $amount, collection_date => $collection_date, creditor_bic => $creditor_bic, debtor_bic => $debtor_bic, description => $description)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CreateSepaDirectDebitApi;
my $api_instance = WWW::OpenAPIClient::CreateSepaDirectDebitApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $creditor_name = "creditor_name_example"; # string | 
my $creditor_iban = "creditor_iban_example"; # string | 
my $creditor_id = "creditor_id_example"; # string | 
my $mandate_id = "mandate_id_example"; # string | 
my $mandate_date = "mandate_date_example"; # string | 
my $debtor_name = "debtor_name_example"; # string | 
my $debtor_iban = "debtor_iban_example"; # string | 
my $amount = "amount_example"; # string | 
my $collection_date = "collection_date_example"; # string | 
my $creditor_bic = "creditor_bic_example"; # string | 
my $debtor_bic = "debtor_bic_example"; # string | 
my $description = "description_example"; # string | 

eval {
    my $result = $api_instance->create_sepa_direct_debit_api(creditor_name => $creditor_name, creditor_iban => $creditor_iban, creditor_id => $creditor_id, mandate_id => $mandate_id, mandate_date => $mandate_date, debtor_name => $debtor_name, debtor_iban => $debtor_iban, amount => $amount, collection_date => $collection_date, creditor_bic => $creditor_bic, debtor_bic => $debtor_bic, description => $description);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CreateSepaDirectDebitApi->create_sepa_direct_debit_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **creditor_name** | **string**|  | 
 **creditor_iban** | **string**|  | 
 **creditor_id** | **string**|  | 
 **mandate_id** | **string**|  | 
 **mandate_date** | **string**|  | 
 **debtor_name** | **string**|  | 
 **debtor_iban** | **string**|  | 
 **amount** | **string**|  | 
 **collection_date** | **string**|  | 
 **creditor_bic** | **string**|  | [optional] 
 **debtor_bic** | **string**|  | [optional] 
 **description** | **string**|  | [optional] 

### Return type

[**SepaDirectDebitResponse**](SepaDirectDebitResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

