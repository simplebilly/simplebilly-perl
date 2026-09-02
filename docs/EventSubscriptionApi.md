# WWW::OpenAPIClient::EventSubscriptionApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::EventSubscriptionApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_event_subscription**](EventSubscriptionApi.md#create_event_subscription) | **POST** /api/v1/event-subscriptions | 
[**delete_event_subscription**](EventSubscriptionApi.md#delete_event_subscription) | **DELETE** /api/v1/event-subscriptions/{subscription_id} | 
[**list_event_subscriptions**](EventSubscriptionApi.md#list_event_subscriptions) | **GET** /api/v1/event-subscriptions/ | 


# **create_event_subscription**
> EventSubscription create_event_subscription(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EventSubscriptionApi;
my $api_instance = WWW::OpenAPIClient::EventSubscriptionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->create_event_subscription(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EventSubscriptionApi->create_event_subscription: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**EventSubscription**](EventSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_event_subscription**
> delete_event_subscription(subscription_id => $subscription_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EventSubscriptionApi;
my $api_instance = WWW::OpenAPIClient::EventSubscriptionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $subscription_id = "subscription_id_example"; # string | 

eval {
    $api_instance->delete_event_subscription(subscription_id => $subscription_id);
};
if ($@) {
    warn "Exception when calling EventSubscriptionApi->delete_event_subscription: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_event_subscriptions**
> ARRAY[EventSubscription] list_event_subscriptions()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EventSubscriptionApi;
my $api_instance = WWW::OpenAPIClient::EventSubscriptionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_event_subscriptions();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EventSubscriptionApi->list_event_subscriptions: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[EventSubscription]**](EventSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

