# WWW::OpenAPIClient::GenerateXrechnungApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GenerateXrechnungApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generate_xrechnung_api**](GenerateXrechnungApi.md#generate_xrechnung_api) | **GET** /api/v1/invoices/{id}/xrechnung | 


# **generate_xrechnung_api**
> XRechnungResponse generate_xrechnung_api(id => $id, supplier_name => $supplier_name, supplier_street => $supplier_street, supplier_city => $supplier_city, supplier_zip => $supplier_zip, supplier_country => $supplier_country, supplier_vat_id => $supplier_vat_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GenerateXrechnungApi;
my $api_instance = WWW::OpenAPIClient::GenerateXrechnungApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $supplier_name = "supplier_name_example"; # string | 
my $supplier_street = "supplier_street_example"; # string | 
my $supplier_city = "supplier_city_example"; # string | 
my $supplier_zip = "supplier_zip_example"; # string | 
my $supplier_country = "supplier_country_example"; # string | 
my $supplier_vat_id = "supplier_vat_id_example"; # string | 

eval {
    my $result = $api_instance->generate_xrechnung_api(id => $id, supplier_name => $supplier_name, supplier_street => $supplier_street, supplier_city => $supplier_city, supplier_zip => $supplier_zip, supplier_country => $supplier_country, supplier_vat_id => $supplier_vat_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GenerateXrechnungApi->generate_xrechnung_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **supplier_name** | **string**|  | [optional] 
 **supplier_street** | **string**|  | [optional] 
 **supplier_city** | **string**|  | [optional] 
 **supplier_zip** | **string**|  | [optional] 
 **supplier_country** | **string**|  | [optional] 
 **supplier_vat_id** | **string**|  | [optional] 

### Return type

[**XRechnungResponse**](XRechnungResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

