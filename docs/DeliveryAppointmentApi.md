# WWW::OpenAPIClient::DeliveryAppointmentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DeliveryAppointmentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_delivery_appointment**](DeliveryAppointmentApi.md#create_delivery_appointment) | **POST** /api/v1/delivery-appointments | 
[**delete_delivery_appointment**](DeliveryAppointmentApi.md#delete_delivery_appointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} | 
[**get_delivery_appointment**](DeliveryAppointmentApi.md#get_delivery_appointment) | **GET** /api/v1/delivery-appointments/{appointment_id} | 
[**get_public_delivery_appointment_status**](DeliveryAppointmentApi.md#get_public_delivery_appointment_status) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
[**list_delivery_appointments**](DeliveryAppointmentApi.md#list_delivery_appointments) | **GET** /api/v1/delivery-appointments | 
[**request_public_delivery_appointment**](DeliveryAppointmentApi.md#request_public_delivery_appointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request.
[**update_delivery_appointment**](DeliveryAppointmentApi.md#update_delivery_appointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} | 
[**update_delivery_appointment_status**](DeliveryAppointmentApi.md#update_delivery_appointment_status) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status | 


# **create_delivery_appointment**
> DeliveryAppointment create_delivery_appointment(delivery_appointment_create => $delivery_appointment_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_appointment_create = WWW::OpenAPIClient::Object::DeliveryAppointmentCreate->new(); # DeliveryAppointmentCreate | 

eval {
    my $result = $api_instance->create_delivery_appointment(delivery_appointment_create => $delivery_appointment_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->create_delivery_appointment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_appointment_create** | [**DeliveryAppointmentCreate**](DeliveryAppointmentCreate.md)|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_delivery_appointment**
> delete_delivery_appointment(appointment_id => $appointment_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $appointment_id = "appointment_id_example"; # string | 

eval {
    $api_instance->delete_delivery_appointment(appointment_id => $appointment_id);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->delete_delivery_appointment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointment_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_delivery_appointment**
> DeliveryAppointment get_delivery_appointment(appointment_id => $appointment_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $appointment_id = "appointment_id_example"; # string | 

eval {
    my $result = $api_instance->get_delivery_appointment(appointment_id => $appointment_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->get_delivery_appointment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointment_id** | **string**|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_public_delivery_appointment_status**
> PublicDeliveryAppointmentStatusResponse get_public_delivery_appointment_status(appointment_id => $appointment_id, email => $email, token => $token)

Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $appointment_id = "appointment_id_example"; # string | 
my $email = "email_example"; # string | 
my $token = "token_example"; # string | 

eval {
    my $result = $api_instance->get_public_delivery_appointment_status(appointment_id => $appointment_id, email => $email, token => $token);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->get_public_delivery_appointment_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointment_id** | **string**|  | 
 **email** | **string**|  | 
 **token** | **string**|  | 

### Return type

[**PublicDeliveryAppointmentStatusResponse**](PublicDeliveryAppointmentStatusResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_delivery_appointments**
> ARRAY[DeliveryAppointment] list_delivery_appointments(page => $page, page_size => $page_size, status => $status, warehouse_id => $warehouse_id, from => $from, to => $to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $warehouse_id = "warehouse_id_example"; # string | 
my $from = DateTime->from_epoch(epoch => str2time('null')); # DATE | 
my $to = DateTime->from_epoch(epoch => str2time('null')); # DATE | 

eval {
    my $result = $api_instance->list_delivery_appointments(page => $page, page_size => $page_size, status => $status, warehouse_id => $warehouse_id, from => $from, to => $to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->list_delivery_appointments: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **warehouse_id** | **string**|  | [optional] 
 **from** | **DATE**|  | [optional] 
 **to** | **DATE**|  | [optional] 

### Return type

[**ARRAY[DeliveryAppointment]**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **request_public_delivery_appointment**
> PublicDeliveryAppointmentResponse request_public_delivery_appointment(public_delivery_appointment_request => $public_delivery_appointment_request)

Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $public_delivery_appointment_request = WWW::OpenAPIClient::Object::PublicDeliveryAppointmentRequest->new(); # PublicDeliveryAppointmentRequest | 

eval {
    my $result = $api_instance->request_public_delivery_appointment(public_delivery_appointment_request => $public_delivery_appointment_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->request_public_delivery_appointment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **public_delivery_appointment_request** | [**PublicDeliveryAppointmentRequest**](PublicDeliveryAppointmentRequest.md)|  | 

### Return type

[**PublicDeliveryAppointmentResponse**](PublicDeliveryAppointmentResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_delivery_appointment**
> DeliveryAppointment update_delivery_appointment(appointment_id => $appointment_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $appointment_id = "appointment_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_delivery_appointment(appointment_id => $appointment_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->update_delivery_appointment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointment_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_delivery_appointment_status**
> DeliveryAppointment update_delivery_appointment_status(appointment_id => $appointment_id, appointment_status_update => $appointment_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryAppointmentApi;
my $api_instance = WWW::OpenAPIClient::DeliveryAppointmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $appointment_id = "appointment_id_example"; # string | 
my $appointment_status_update = WWW::OpenAPIClient::Object::AppointmentStatusUpdate->new(); # AppointmentStatusUpdate | 

eval {
    my $result = $api_instance->update_delivery_appointment_status(appointment_id => $appointment_id, appointment_status_update => $appointment_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryAppointmentApi->update_delivery_appointment_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **appointment_id** | **string**|  | 
 **appointment_status_update** | [**AppointmentStatusUpdate**](AppointmentStatusUpdate.md)|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

