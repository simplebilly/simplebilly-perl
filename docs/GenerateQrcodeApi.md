# WWW::OpenAPIClient::GenerateQrcodeApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GenerateQrcodeApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generate_qrcode_api**](GenerateQrcodeApi.md#generate_qrcode_api) | **GET** /api/v1/invoices/{id}/qrcode | 


# **generate_qrcode_api**
> QRCodeResponse generate_qrcode_api(iban => $iban, id => $id, holder_name => $holder_name, bic => $bic, amount => $amount, reference => $reference, purpose => $purpose)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GenerateQrcodeApi;
my $api_instance = WWW::OpenAPIClient::GenerateQrcodeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $iban = "iban_example"; # string | 
my $id = "id_example"; # string | 
my $holder_name = "holder_name_example"; # string | 
my $bic = "bic_example"; # string | 
my $amount = "amount_example"; # string | 
my $reference = "reference_example"; # string | 
my $purpose = "purpose_example"; # string | 

eval {
    my $result = $api_instance->generate_qrcode_api(iban => $iban, id => $id, holder_name => $holder_name, bic => $bic, amount => $amount, reference => $reference, purpose => $purpose);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GenerateQrcodeApi->generate_qrcode_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **iban** | **string**|  | 
 **id** | **string**|  | 
 **holder_name** | **string**|  | [optional] 
 **bic** | **string**|  | [optional] 
 **amount** | **string**|  | [optional] 
 **reference** | **string**|  | [optional] 
 **purpose** | **string**|  | [optional] 

### Return type

[**QRCodeResponse**](QRCodeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

