# WWW::OpenAPIClient::PaymentConditionApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PaymentConditionApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_payment_conditions_api**](PaymentConditionApi.md#list_payment_conditions_api) | **GET** /api/v1/payment-conditions | 


# **list_payment_conditions_api**
> ARRAY[PaymentCondition] list_payment_conditions_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentConditionApi;
my $api_instance = WWW::OpenAPIClient::PaymentConditionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_payment_conditions_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentConditionApi->list_payment_conditions_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[PaymentCondition]**](PaymentCondition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

