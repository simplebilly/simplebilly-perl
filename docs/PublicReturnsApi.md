# WWW::OpenAPIClient::PublicReturnsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PublicReturnsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_public_return_status**](PublicReturnsApi.md#get_public_return_status) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.
[**list_public_returns**](PublicReturnsApi.md#list_public_returns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth).
[**request_public_return**](PublicReturnsApi.md#request_public_return) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth).


# **get_public_return_status**
> PublicReturnStatusResponse get_public_return_status(email => $email, return_number => $return_number, return_order_id => $return_order_id, order_number => $order_number)

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PublicReturnsApi;
my $api_instance = WWW::OpenAPIClient::PublicReturnsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $email = "email_example"; # string | 
my $return_number = "return_number_example"; # string | Either return_number or return_order_id must be provided.
my $return_order_id = "return_order_id_example"; # string | 
my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->get_public_return_status(email => $email, return_number => $return_number, return_order_id => $return_order_id, order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PublicReturnsApi->get_public_return_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **email** | **string**|  | 
 **return_number** | **string**| Either return_number or return_order_id must be provided. | [optional] 
 **return_order_id** | **string**|  | [optional] 
 **order_number** | **string**|  | [optional] 

### Return type

[**PublicReturnStatusResponse**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_public_returns**
> ARRAY[PublicReturnStatusResponse] list_public_returns(order_number => $order_number, email => $email)

List all returns for an order (public, no auth).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PublicReturnsApi;
my $api_instance = WWW::OpenAPIClient::PublicReturnsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 
my $email = "email_example"; # string | 

eval {
    my $result = $api_instance->list_public_returns(order_number => $order_number, email => $email);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PublicReturnsApi->list_public_returns: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 
 **email** | **string**|  | 

### Return type

[**ARRAY[PublicReturnStatusResponse]**](PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **request_public_return**
> PublicReturnResponse request_public_return(public_return_request => $public_return_request)

Customer requests a return for an order (public, no auth).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PublicReturnsApi;
my $api_instance = WWW::OpenAPIClient::PublicReturnsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $public_return_request = WWW::OpenAPIClient::Object::PublicReturnRequest->new(); # PublicReturnRequest | 

eval {
    my $result = $api_instance->request_public_return(public_return_request => $public_return_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PublicReturnsApi->request_public_return: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **public_return_request** | [**PublicReturnRequest**](PublicReturnRequest.md)|  | 

### Return type

[**PublicReturnResponse**](PublicReturnResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

