# WWW::OpenAPIClient::BillingApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::BillingApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_plans**](BillingApi.md#get_plans) | **GET** /api/v1/plans | All canonical plans (free/starter/business/enterprise) — the single source of truth lives in &#x60;crate::saasy::plans&#x60;, matching marketing.
[**get_quota_api**](BillingApi.md#get_quota_api) | **GET** /api/v1/quota | Effective limits + current usage for the calling tenant.
[**get_subscription_api**](BillingApi.md#get_subscription_api) | **GET** /api/v1/subscription | 
[**get_usage_api**](BillingApi.md#get_usage_api) | **GET** /api/v1/usage | 
[**paddle_subscription_webhook**](BillingApi.md#paddle_subscription_webhook) | **POST** /api/webhooks/paddle/subscription | Paddle Billing subscription webhook. Verifies the &#x60;Paddle-Signature&#x60; header (HMAC-SHA256 over &#x60;\&quot;{ts}:{raw_body}\&quot;&#x60; with the webhook secret), then updates &#x60;billing_info&#x60; and &#x60;tenants.plan&#x60; for the tenant identified by the subscription &#x60;custom_data&#x60; (JSON &#x60;{\&quot;tenant_id\&quot;: \&quot;...\&quot;}&#x60; or a bare tenant UUID).
[**put_quota_api**](BillingApi.md#put_quota_api) | **PUT** /api/v1/quota | Write the per-tenant quota override (&#x60;admin:settings&#x60;). An empty object clears the override.


# **get_plans**
> ApiResponseVecPlan get_plans()

All canonical plans (free/starter/business/enterprise) — the single source of truth lives in `crate::saasy::plans`, matching marketing.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BillingApi;
my $api_instance = WWW::OpenAPIClient::BillingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_plans();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BillingApi->get_plans: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseVecPlan**](ApiResponseVecPlan.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_quota_api**
> get_quota_api()

Effective limits + current usage for the calling tenant.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BillingApi;
my $api_instance = WWW::OpenAPIClient::BillingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    $api_instance->get_quota_api();
};
if ($@) {
    warn "Exception when calling BillingApi->get_quota_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_subscription_api**
> ApiResponseSubscriptionOverview get_subscription_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BillingApi;
my $api_instance = WWW::OpenAPIClient::BillingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_subscription_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BillingApi->get_subscription_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseSubscriptionOverview**](ApiResponseSubscriptionOverview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_usage_api**
> get_usage_api(meter => $meter)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BillingApi;
my $api_instance = WWW::OpenAPIClient::BillingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $meter = "meter_example"; # string | 

eval {
    $api_instance->get_usage_api(meter => $meter);
};
if ($@) {
    warn "Exception when calling BillingApi->get_usage_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **meter** | **string**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paddle_subscription_webhook**
> paddle_subscription_webhook()

Paddle Billing subscription webhook. Verifies the `Paddle-Signature` header (HMAC-SHA256 over `\"{ts}:{raw_body}\"` with the webhook secret), then updates `billing_info` and `tenants.plan` for the tenant identified by the subscription `custom_data` (JSON `{\"tenant_id\": \"...\"}` or a bare tenant UUID).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BillingApi;
my $api_instance = WWW::OpenAPIClient::BillingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    $api_instance->paddle_subscription_webhook();
};
if ($@) {
    warn "Exception when calling BillingApi->paddle_subscription_webhook: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_quota_api**
> put_quota_api(quota_override => $quota_override)

Write the per-tenant quota override (`admin:settings`). An empty object clears the override.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BillingApi;
my $api_instance = WWW::OpenAPIClient::BillingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quota_override = WWW::OpenAPIClient::Object::QuotaOverride->new(); # QuotaOverride | 

eval {
    $api_instance->put_quota_api(quota_override => $quota_override);
};
if ($@) {
    warn "Exception when calling BillingApi->put_quota_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quota_override** | [**QuotaOverride**](QuotaOverride.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

