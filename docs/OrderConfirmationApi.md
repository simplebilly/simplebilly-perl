# WWW::OpenAPIClient::OrderConfirmationApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::OrderConfirmationApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_confirmation**](OrderConfirmationApi.md#create_confirmation) | **POST** /api/v1/order-confirmations | 
[**delete_confirmation**](OrderConfirmationApi.md#delete_confirmation) | **DELETE** /api/v1/order-confirmations/{confirmation_id} | 
[**download_confirmation_pdf**](OrderConfirmationApi.md#download_confirmation_pdf) | **GET** /api/v1/order-confirmations/{confirmation_id}/pdf | 
[**get_confirmation**](OrderConfirmationApi.md#get_confirmation) | **GET** /api/v1/order-confirmations/{confirmation_id} | 
[**list_confirmations**](OrderConfirmationApi.md#list_confirmations) | **GET** /api/v1/order-confirmations/ | 
[**orderconfirmation_restore**](OrderConfirmationApi.md#orderconfirmation_restore) | **POST** /api/v1/order-confirmations/{confirmation_id}/restore | 
[**pursue_confirmation**](OrderConfirmationApi.md#pursue_confirmation) | **POST** /api/v1/order-confirmations/{confirmation_id}/pursue | 


# **create_confirmation**
> OrderConfirmation create_confirmation(order_confirmation_create => $order_confirmation_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderConfirmationApi;
my $api_instance = WWW::OpenAPIClient::OrderConfirmationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_confirmation_create = WWW::OpenAPIClient::Object::OrderConfirmationCreate->new(); # OrderConfirmationCreate | 

eval {
    my $result = $api_instance->create_confirmation(order_confirmation_create => $order_confirmation_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderConfirmationApi->create_confirmation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_confirmation_create** | [**OrderConfirmationCreate**](OrderConfirmationCreate.md)|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_confirmation**
> delete_confirmation(confirmation_id => $confirmation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderConfirmationApi;
my $api_instance = WWW::OpenAPIClient::OrderConfirmationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $confirmation_id = "confirmation_id_example"; # string | 

eval {
    $api_instance->delete_confirmation(confirmation_id => $confirmation_id);
};
if ($@) {
    warn "Exception when calling OrderConfirmationApi->delete_confirmation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirmation_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_confirmation_pdf**
> download_confirmation_pdf(confirmation_id => $confirmation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderConfirmationApi;
my $api_instance = WWW::OpenAPIClient::OrderConfirmationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $confirmation_id = "confirmation_id_example"; # string | 

eval {
    $api_instance->download_confirmation_pdf(confirmation_id => $confirmation_id);
};
if ($@) {
    warn "Exception when calling OrderConfirmationApi->download_confirmation_pdf: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirmation_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_confirmation**
> OrderConfirmation get_confirmation(confirmation_id => $confirmation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderConfirmationApi;
my $api_instance = WWW::OpenAPIClient::OrderConfirmationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $confirmation_id = "confirmation_id_example"; # string | 

eval {
    my $result = $api_instance->get_confirmation(confirmation_id => $confirmation_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderConfirmationApi->get_confirmation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirmation_id** | **string**|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_confirmations**
> ARRAY[OrderConfirmation] list_confirmations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderConfirmationApi;
my $api_instance = WWW::OpenAPIClient::OrderConfirmationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->list_confirmations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderConfirmationApi->list_confirmations: $@\n";
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

[**ARRAY[OrderConfirmation]**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **orderconfirmation_restore**
> OrderConfirmation orderconfirmation_restore(confirmation_id => $confirmation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderConfirmationApi;
my $api_instance = WWW::OpenAPIClient::OrderConfirmationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $confirmation_id = "confirmation_id_example"; # string | 

eval {
    my $result = $api_instance->orderconfirmation_restore(confirmation_id => $confirmation_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderConfirmationApi->orderconfirmation_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirmation_id** | **string**|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pursue_confirmation**
> DeliveryNote pursue_confirmation(confirmation_id => $confirmation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OrderConfirmationApi;
my $api_instance = WWW::OpenAPIClient::OrderConfirmationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $confirmation_id = "confirmation_id_example"; # string | 

eval {
    my $result = $api_instance->pursue_confirmation(confirmation_id => $confirmation_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OrderConfirmationApi->pursue_confirmation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **confirmation_id** | **string**|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

