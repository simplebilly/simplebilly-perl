# WWW::OpenAPIClient::PaymentGatewayApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PaymentGatewayApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_payment_gateway_api**](PaymentGatewayApi.md#create_payment_gateway_api) | **POST** /api/v1/payment-gateways | 
[**delete_payment_gateway_api**](PaymentGatewayApi.md#delete_payment_gateway_api) | **DELETE** /api/v1/payment-gateways/{gateway_id} | 
[**list_payment_gateways_api**](PaymentGatewayApi.md#list_payment_gateways_api) | **GET** /api/v1/payment-gateways/ | 
[**oauth_authorize_api**](PaymentGatewayApi.md#oauth_authorize_api) | **POST** /api/v1/payment-gateways/oauth/authorize | 
[**oauth_callback_api**](PaymentGatewayApi.md#oauth_callback_api) | **POST** /api/v1/payment-gateways/oauth/callback | 
[**update_payment_gateway_api**](PaymentGatewayApi.md#update_payment_gateway_api) | **PUT** /api/v1/payment-gateways/{gateway_id} | 


# **create_payment_gateway_api**
> PaymentGateway create_payment_gateway_api(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentGatewayApi;
my $api_instance = WWW::OpenAPIClient::PaymentGatewayApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->create_payment_gateway_api(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentGatewayApi->create_payment_gateway_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_payment_gateway_api**
> delete_payment_gateway_api(gateway_id => $gateway_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentGatewayApi;
my $api_instance = WWW::OpenAPIClient::PaymentGatewayApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $gateway_id = "gateway_id_example"; # string | 

eval {
    $api_instance->delete_payment_gateway_api(gateway_id => $gateway_id);
};
if ($@) {
    warn "Exception when calling PaymentGatewayApi->delete_payment_gateway_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **gateway_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_payment_gateways_api**
> ARRAY[PaymentGateway] list_payment_gateways_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentGatewayApi;
my $api_instance = WWW::OpenAPIClient::PaymentGatewayApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_payment_gateways_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentGatewayApi->list_payment_gateways_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[PaymentGateway]**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_authorize_api**
> GatewayOAuthAuthorizeResponse oauth_authorize_api(gateway_o_auth_authorize_request => $gateway_o_auth_authorize_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentGatewayApi;
my $api_instance = WWW::OpenAPIClient::PaymentGatewayApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $gateway_o_auth_authorize_request = WWW::OpenAPIClient::Object::GatewayOAuthAuthorizeRequest->new(); # GatewayOAuthAuthorizeRequest | 

eval {
    my $result = $api_instance->oauth_authorize_api(gateway_o_auth_authorize_request => $gateway_o_auth_authorize_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentGatewayApi->oauth_authorize_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **gateway_o_auth_authorize_request** | [**GatewayOAuthAuthorizeRequest**](GatewayOAuthAuthorizeRequest.md)|  | 

### Return type

[**GatewayOAuthAuthorizeResponse**](GatewayOAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_callback_api**
> PaymentGateway oauth_callback_api(gateway_o_auth_callback_request => $gateway_o_auth_callback_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentGatewayApi;
my $api_instance = WWW::OpenAPIClient::PaymentGatewayApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $gateway_o_auth_callback_request = WWW::OpenAPIClient::Object::GatewayOAuthCallbackRequest->new(); # GatewayOAuthCallbackRequest | 

eval {
    my $result = $api_instance->oauth_callback_api(gateway_o_auth_callback_request => $gateway_o_auth_callback_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentGatewayApi->oauth_callback_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **gateway_o_auth_callback_request** | [**GatewayOAuthCallbackRequest**](GatewayOAuthCallbackRequest.md)|  | 

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_payment_gateway_api**
> PaymentGateway update_payment_gateway_api(gateway_id => $gateway_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentGatewayApi;
my $api_instance = WWW::OpenAPIClient::PaymentGatewayApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $gateway_id = "gateway_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_payment_gateway_api(gateway_id => $gateway_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentGatewayApi->update_payment_gateway_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **gateway_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**PaymentGateway**](PaymentGateway.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

