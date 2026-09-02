# WWW::OpenAPIClient::TaxApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::TaxApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_tax_rate**](TaxApi.md#create_tax_rate) | **POST** /api/v1/tax-rates | Create a tax rate (&#x60;admin:settings&#x60;).
[**delete_tax_rate**](TaxApi.md#delete_tax_rate) | **DELETE** /api/v1/tax-rates/{id} | Delete a tax rate by id (&#x60;admin:settings&#x60;).
[**list_tax_rates**](TaxApi.md#list_tax_rates) | **GET** /api/v1/tax-rates | List the calling tenant&#39;s tax rates.
[**update_tax_rate**](TaxApi.md#update_tax_rate) | **PUT** /api/v1/tax-rates/{id} | Update a tax rate by id (&#x60;admin:settings&#x60;). Replaces all body fields.


# **create_tax_rate**
> create_tax_rate(tax_rate_create => $tax_rate_create)

Create a tax rate (`admin:settings`).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TaxApi;
my $api_instance = WWW::OpenAPIClient::TaxApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $tax_rate_create = WWW::OpenAPIClient::Object::TaxRateCreate->new(); # TaxRateCreate | 

eval {
    $api_instance->create_tax_rate(tax_rate_create => $tax_rate_create);
};
if ($@) {
    warn "Exception when calling TaxApi->create_tax_rate: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tax_rate_create** | [**TaxRateCreate**](TaxRateCreate.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_tax_rate**
> delete_tax_rate(id => $id)

Delete a tax rate by id (`admin:settings`).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TaxApi;
my $api_instance = WWW::OpenAPIClient::TaxApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_tax_rate(id => $id);
};
if ($@) {
    warn "Exception when calling TaxApi->delete_tax_rate: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_tax_rates**
> list_tax_rates()

List the calling tenant's tax rates.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TaxApi;
my $api_instance = WWW::OpenAPIClient::TaxApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    $api_instance->list_tax_rates();
};
if ($@) {
    warn "Exception when calling TaxApi->list_tax_rates: $@\n";
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

# **update_tax_rate**
> update_tax_rate(id => $id, tax_rate_create => $tax_rate_create)

Update a tax rate by id (`admin:settings`). Replaces all body fields.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TaxApi;
my $api_instance = WWW::OpenAPIClient::TaxApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $tax_rate_create = WWW::OpenAPIClient::Object::TaxRateCreate->new(); # TaxRateCreate | 

eval {
    $api_instance->update_tax_rate(id => $id, tax_rate_create => $tax_rate_create);
};
if ($@) {
    warn "Exception when calling TaxApi->update_tax_rate: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **tax_rate_create** | [**TaxRateCreate**](TaxRateCreate.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

