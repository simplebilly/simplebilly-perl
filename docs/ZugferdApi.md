# WWW::OpenAPIClient::ZugferdApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ZugferdApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generate_zugferd_api**](ZugferdApi.md#generate_zugferd_api) | **GET** /api/v1/invoices/{id}/zugferd | 


# **generate_zugferd_api**
> generate_zugferd_api(id => $id, supplier_name => $supplier_name, supplier_street => $supplier_street, supplier_city => $supplier_city, supplier_zip => $supplier_zip, supplier_country => $supplier_country, supplier_vat_id => $supplier_vat_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ZugferdApi;
my $api_instance = WWW::OpenAPIClient::ZugferdApi->new(

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
    $api_instance->generate_zugferd_api(id => $id, supplier_name => $supplier_name, supplier_street => $supplier_street, supplier_city => $supplier_city, supplier_zip => $supplier_zip, supplier_country => $supplier_country, supplier_vat_id => $supplier_vat_id);
};
if ($@) {
    warn "Exception when calling ZugferdApi->generate_zugferd_api: $@\n";
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

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

