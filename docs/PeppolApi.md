# WWW::OpenAPIClient::PeppolApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PeppolApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**peppol_api**](PeppolApi.md#peppol_api) | **GET** /api/v1/invoices/{id}/peppol | 


# **peppol_api**
> PeppolResponse peppol_api(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PeppolApi;
my $api_instance = WWW::OpenAPIClient::PeppolApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->peppol_api(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PeppolApi->peppol_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**PeppolResponse**](PeppolResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

