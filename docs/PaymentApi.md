# WWW::OpenAPIClient::PaymentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PaymentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_payment**](PaymentApi.md#create_payment) | **POST** /api/v1/payments | 
[**delete_payment**](PaymentApi.md#delete_payment) | **DELETE** /api/v1/payments/{id} | 
[**get_payment**](PaymentApi.md#get_payment) | **GET** /api/v1/payments/{id} | 
[**get_payments**](PaymentApi.md#get_payments) | **GET** /api/v1/payments/ | 
[**payment_restore**](PaymentApi.md#payment_restore) | **POST** /api/v1/payments/{id}/restore | 
[**update_payment**](PaymentApi.md#update_payment) | **PUT** /api/v1/payments/{id} | 


# **create_payment**
> Payment create_payment(payment_create => $payment_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentApi;
my $api_instance = WWW::OpenAPIClient::PaymentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $payment_create = WWW::OpenAPIClient::Object::PaymentCreate->new(); # PaymentCreate | 

eval {
    my $result = $api_instance->create_payment(payment_create => $payment_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentApi->create_payment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payment_create** | [**PaymentCreate**](PaymentCreate.md)|  | 

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_payment**
> delete_payment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentApi;
my $api_instance = WWW::OpenAPIClient::PaymentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_payment(id => $id);
};
if ($@) {
    warn "Exception when calling PaymentApi->delete_payment: $@\n";
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
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_payment**
> Payment get_payment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentApi;
my $api_instance = WWW::OpenAPIClient::PaymentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_payment(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentApi->get_payment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_payments**
> ARRAY[Payment] get_payments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentApi;
my $api_instance = WWW::OpenAPIClient::PaymentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_payments(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentApi->get_payments: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **include_deleted** | **boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**ARRAY[Payment]**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payment_restore**
> Payment payment_restore(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentApi;
my $api_instance = WWW::OpenAPIClient::PaymentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->payment_restore(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentApi->payment_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_payment**
> Payment update_payment(id => $id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PaymentApi;
my $api_instance = WWW::OpenAPIClient::PaymentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_payment(id => $id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PaymentApi->update_payment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Payment**](Payment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

