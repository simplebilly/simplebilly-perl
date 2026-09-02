# WWW::OpenAPIClient::DeliveryDateApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DeliveryDateApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_delivery_date**](DeliveryDateApi.md#create_delivery_date) | **POST** /api/v1/delivery-dates | 
[**delete_delivery_date**](DeliveryDateApi.md#delete_delivery_date) | **DELETE** /api/v1/delivery-dates/{delivery_date_id} | 
[**get_delivery_date**](DeliveryDateApi.md#get_delivery_date) | **GET** /api/v1/delivery-dates/{delivery_date_id} | 
[**get_delivery_performance**](DeliveryDateApi.md#get_delivery_performance) | **GET** /api/v1/delivery-dates/performance | On-time performance summary: how many promised delivery dates were met within a period.
[**list_delivery_dates**](DeliveryDateApi.md#list_delivery_dates) | **GET** /api/v1/delivery-dates/ | 
[**update_delivery_date**](DeliveryDateApi.md#update_delivery_date) | **PUT** /api/v1/delivery-dates/{delivery_date_id} | 
[**update_delivery_date_status**](DeliveryDateApi.md#update_delivery_date_status) | **PUT** /api/v1/delivery-dates/{delivery_date_id}/status | 


# **create_delivery_date**
> DeliveryDate create_delivery_date(delivery_date_create => $delivery_date_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryDateApi;
my $api_instance = WWW::OpenAPIClient::DeliveryDateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_date_create = WWW::OpenAPIClient::Object::DeliveryDateCreate->new(); # DeliveryDateCreate | 

eval {
    my $result = $api_instance->create_delivery_date(delivery_date_create => $delivery_date_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryDateApi->create_delivery_date: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_date_create** | [**DeliveryDateCreate**](DeliveryDateCreate.md)|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_delivery_date**
> delete_delivery_date(delivery_date_id => $delivery_date_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryDateApi;
my $api_instance = WWW::OpenAPIClient::DeliveryDateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_date_id = "delivery_date_id_example"; # string | 

eval {
    $api_instance->delete_delivery_date(delivery_date_id => $delivery_date_id);
};
if ($@) {
    warn "Exception when calling DeliveryDateApi->delete_delivery_date: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_date_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_delivery_date**
> DeliveryDate get_delivery_date(delivery_date_id => $delivery_date_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryDateApi;
my $api_instance = WWW::OpenAPIClient::DeliveryDateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_date_id = "delivery_date_id_example"; # string | 

eval {
    my $result = $api_instance->get_delivery_date(delivery_date_id => $delivery_date_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryDateApi->get_delivery_date: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_date_id** | **string**|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_delivery_performance**
> object get_delivery_performance(page => $page, page_size => $page_size, order_number => $order_number, status => $status, from => $from, to => $to)

On-time performance summary: how many promised delivery dates were met within a period.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryDateApi;
my $api_instance = WWW::OpenAPIClient::DeliveryDateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $order_number = "order_number_example"; # string | 
my $status = "status_example"; # string | 
my $from = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only dates on or after this date.
my $to = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only dates on or before this date.

eval {
    my $result = $api_instance->get_delivery_performance(page => $page, page_size => $page_size, order_number => $order_number, status => $status, from => $from, to => $to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryDateApi->get_delivery_performance: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **order_number** | **string**|  | [optional] 
 **status** | **string**|  | [optional] 
 **from** | **DATE**| Only dates on or after this date. | [optional] 
 **to** | **DATE**| Only dates on or before this date. | [optional] 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_delivery_dates**
> ARRAY[DeliveryDate] list_delivery_dates(page => $page, page_size => $page_size, order_number => $order_number, status => $status, from => $from, to => $to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryDateApi;
my $api_instance = WWW::OpenAPIClient::DeliveryDateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $order_number = "order_number_example"; # string | 
my $status = "status_example"; # string | 
my $from = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only dates on or after this date.
my $to = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only dates on or before this date.

eval {
    my $result = $api_instance->list_delivery_dates(page => $page, page_size => $page_size, order_number => $order_number, status => $status, from => $from, to => $to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryDateApi->list_delivery_dates: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **order_number** | **string**|  | [optional] 
 **status** | **string**|  | [optional] 
 **from** | **DATE**| Only dates on or after this date. | [optional] 
 **to** | **DATE**| Only dates on or before this date. | [optional] 

### Return type

[**ARRAY[DeliveryDate]**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_delivery_date**
> DeliveryDate update_delivery_date(delivery_date_id => $delivery_date_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryDateApi;
my $api_instance = WWW::OpenAPIClient::DeliveryDateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_date_id = "delivery_date_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_delivery_date(delivery_date_id => $delivery_date_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryDateApi->update_delivery_date: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_date_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_delivery_date_status**
> DeliveryDate update_delivery_date_status(delivery_date_id => $delivery_date_id, delivery_date_status_update => $delivery_date_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryDateApi;
my $api_instance = WWW::OpenAPIClient::DeliveryDateApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_date_id = "delivery_date_id_example"; # string | 
my $delivery_date_status_update = WWW::OpenAPIClient::Object::DeliveryDateStatusUpdate->new(); # DeliveryDateStatusUpdate | 

eval {
    my $result = $api_instance->update_delivery_date_status(delivery_date_id => $delivery_date_id, delivery_date_status_update => $delivery_date_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryDateApi->update_delivery_date_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_date_id** | **string**|  | 
 **delivery_date_status_update** | [**DeliveryDateStatusUpdate**](DeliveryDateStatusUpdate.md)|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

