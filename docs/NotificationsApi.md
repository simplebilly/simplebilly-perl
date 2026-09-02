# WWW::OpenAPIClient::NotificationsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::NotificationsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_notification**](NotificationsApi.md#delete_notification) | **DELETE** /api/v1/notifications/{id} | 
[**list_notifications**](NotificationsApi.md#list_notifications) | **GET** /api/v1/notifications | 
[**mark_all_read**](NotificationsApi.md#mark_all_read) | **PUT** /api/v1/notifications/read-all | 
[**mark_as_read**](NotificationsApi.md#mark_as_read) | **PUT** /api/v1/notifications/{id}/read | 
[**unread_count**](NotificationsApi.md#unread_count) | **GET** /api/v1/notifications/unread-count | 


# **delete_notification**
> delete_notification(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::NotificationsApi;
my $api_instance = WWW::OpenAPIClient::NotificationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_notification(id => $id);
};
if ($@) {
    warn "Exception when calling NotificationsApi->delete_notification: $@\n";
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

# **list_notifications**
> ARRAY[NotificationDto] list_notifications()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::NotificationsApi;
my $api_instance = WWW::OpenAPIClient::NotificationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_notifications();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling NotificationsApi->list_notifications: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[NotificationDto]**](NotificationDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mark_all_read**
> int mark_all_read()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::NotificationsApi;
my $api_instance = WWW::OpenAPIClient::NotificationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->mark_all_read();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling NotificationsApi->mark_all_read: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**int**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mark_as_read**
> mark_as_read(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::NotificationsApi;
my $api_instance = WWW::OpenAPIClient::NotificationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->mark_as_read(id => $id);
};
if ($@) {
    warn "Exception when calling NotificationsApi->mark_as_read: $@\n";
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

# **unread_count**
> int unread_count()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::NotificationsApi;
my $api_instance = WWW::OpenAPIClient::NotificationsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->unread_count();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling NotificationsApi->unread_count: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**int**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

