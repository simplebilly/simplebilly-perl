# WWW::OpenAPIClient::WebhooksApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::WebhooksApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_subscription**](WebhooksApi.md#create_subscription) | **POST** /api/v1/webhook-subscriptions | Create a webhook subscription (outbound hook).
[**delete_subscription**](WebhooksApi.md#delete_subscription) | **DELETE** /api/v1/webhook-subscriptions/{subscription_id} | Delete a webhook subscription.
[**emit_api**](WebhooksApi.md#emit_api) | **POST** /api/v1/webhooks/emit | Manually fire an event against matching hooks (for testing/flows).
[**list_event**](WebhooksApi.md#list_event) | **GET** /api/v1/webhook-events | List webhook events (inbound + outbound log).
[**list_subscriptions**](WebhooksApi.md#list_subscriptions) | **GET** /api/v1/webhook-subscriptions | List webhook subscriptions for the tenant.
[**update_subscription**](WebhooksApi.md#update_subscription) | **PUT** /api/v1/webhook-subscriptions/{subscription_id} | Update a webhook subscription.


# **create_subscription**
> WebhookSubscription create_subscription(create_subscription_request => $create_subscription_request)

Create a webhook subscription (outbound hook).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WebhooksApi;
my $api_instance = WWW::OpenAPIClient::WebhooksApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $create_subscription_request = WWW::OpenAPIClient::Object::CreateSubscriptionRequest->new(); # CreateSubscriptionRequest | 

eval {
    my $result = $api_instance->create_subscription(create_subscription_request => $create_subscription_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WebhooksApi->create_subscription: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_subscription_request** | [**CreateSubscriptionRequest**](CreateSubscriptionRequest.md)|  | 

### Return type

[**WebhookSubscription**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_subscription**
> delete_subscription(subscription_id => $subscription_id)

Delete a webhook subscription.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WebhooksApi;
my $api_instance = WWW::OpenAPIClient::WebhooksApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $subscription_id = "subscription_id_example"; # string | 

eval {
    $api_instance->delete_subscription(subscription_id => $subscription_id);
};
if ($@) {
    warn "Exception when calling WebhooksApi->delete_subscription: $@\n";
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **emit_api**
> emit_api(emit_event_request => $emit_event_request)

Manually fire an event against matching hooks (for testing/flows).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WebhooksApi;
my $api_instance = WWW::OpenAPIClient::WebhooksApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $emit_event_request = WWW::OpenAPIClient::Object::EmitEventRequest->new(); # EmitEventRequest | 

eval {
    $api_instance->emit_api(emit_event_request => $emit_event_request);
};
if ($@) {
    warn "Exception when calling WebhooksApi->emit_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **emit_event_request** | [**EmitEventRequest**](EmitEventRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_event**
> ARRAY[WebhookEvent] list_event()

List webhook events (inbound + outbound log).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WebhooksApi;
my $api_instance = WWW::OpenAPIClient::WebhooksApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_event();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WebhooksApi->list_event: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[WebhookEvent]**](WebhookEvent.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_subscriptions**
> ARRAY[WebhookSubscription] list_subscriptions()

List webhook subscriptions for the tenant.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WebhooksApi;
my $api_instance = WWW::OpenAPIClient::WebhooksApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_subscriptions();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WebhooksApi->list_subscriptions: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[WebhookSubscription]**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_subscription**
> WebhookSubscription update_subscription(subscription_id => $subscription_id, update_subscription_request => $update_subscription_request)

Update a webhook subscription.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::WebhooksApi;
my $api_instance = WWW::OpenAPIClient::WebhooksApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $subscription_id = "subscription_id_example"; # string | 
my $update_subscription_request = WWW::OpenAPIClient::Object::UpdateSubscriptionRequest->new(); # UpdateSubscriptionRequest | 

eval {
    my $result = $api_instance->update_subscription(subscription_id => $subscription_id, update_subscription_request => $update_subscription_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling WebhooksApi->update_subscription: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **subscription_id** | **string**|  | 
 **update_subscription_request** | [**UpdateSubscriptionRequest**](UpdateSubscriptionRequest.md)|  | 

### Return type

[**WebhookSubscription**](WebhookSubscription.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

