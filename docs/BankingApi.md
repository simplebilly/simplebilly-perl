# WWW::OpenAPIClient::BankingApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::BankingApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bank_lookup_api**](BankingApi.md#bank_lookup_api) | **GET** /api/v1/bookkeeping/banking/lookup | 
[**bank_transactions_api**](BankingApi.md#bank_transactions_api) | **GET** /api/v1/bookkeeping/banking/transactions | 
[**hebesatz_lookup_api**](BankingApi.md#hebesatz_lookup_api) | **GET** /api/v1/bookkeeping/hebesatz | 


# **bank_lookup_api**
> BankLookup bank_lookup_api(iban => $iban)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BankingApi;
my $api_instance = WWW::OpenAPIClient::BankingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $iban = "iban_example"; # string | 

eval {
    my $result = $api_instance->bank_lookup_api(iban => $iban);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BankingApi->bank_lookup_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **iban** | **string**|  | 

### Return type

[**BankLookup**](BankLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bank_transactions_api**
> bank_transactions_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BankingApi;
my $api_instance = WWW::OpenAPIClient::BankingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    $api_instance->bank_transactions_api();
};
if ($@) {
    warn "Exception when calling BankingApi->bank_transactions_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **hebesatz_lookup_api**
> ARRAY[HebesatzLookup] hebesatz_lookup_api(gemeindeschluessel => $gemeindeschluessel, plz => $plz, name => $name, stichtag => $stichtag, country_code => $country_code)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BankingApi;
my $api_instance = WWW::OpenAPIClient::BankingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $gemeindeschluessel = "gemeindeschluessel_example"; # string | 
my $plz = "plz_example"; # string | 
my $name = "name_example"; # string | 
my $stichtag = "stichtag_example"; # string | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from <= date <= valid_to.
my $country_code = "country_code_example"; # string | 

eval {
    my $result = $api_instance->hebesatz_lookup_api(gemeindeschluessel => $gemeindeschluessel, plz => $plz, name => $name, stichtag => $stichtag, country_code => $country_code);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BankingApi->hebesatz_lookup_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **gemeindeschluessel** | **string**|  | [optional] 
 **plz** | **string**|  | [optional] 
 **name** | **string**|  | [optional] 
 **stichtag** | **string**| Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from &lt;&#x3D; date &lt;&#x3D; valid_to. | [optional] 
 **country_code** | **string**|  | [optional] 

### Return type

[**ARRAY[HebesatzLookup]**](HebesatzLookup.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

