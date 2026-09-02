# WWW::OpenAPIClient::MarketplaceApiApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::MarketplaceApiApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_connection_api**](MarketplaceApiApi.md#create_connection_api) | **POST** /api/v1/marketplace/connections | Create a new connection (for API-key based platforms)
[**delete_connection_api**](MarketplaceApiApi.md#delete_connection_api) | **DELETE** /api/v1/marketplace/connections/{connection_id} | Soft-delete a connection
[**get_connection_api**](MarketplaceApiApi.md#get_connection_api) | **GET** /api/v1/marketplace/connections/{connection_id} | Get a single connection
[**get_sync_direction_api**](MarketplaceApiApi.md#get_sync_direction_api) | **GET** /api/v1/marketplace/connections/{connection_id}/directions | Get current sync direction configuration for a connection
[**get_sync_logs_api**](MarketplaceApiApi.md#get_sync_logs_api) | **GET** /api/v1/marketplace/connections/{connection_id}/logs | Get sync logs for a connection
[**list_connections_api**](MarketplaceApiApi.md#list_connections_api) | **GET** /api/v1/marketplace/connections | List connections for the current tenant
[**list_platforms_api**](MarketplaceApiApi.md#list_platforms_api) | **GET** /api/v1/marketplace/platforms | List all supported platforms
[**oauth_authorize_api**](MarketplaceApiApi.md#oauth_authorize_api) | **POST** /api/v1/marketplace/oauth/authorize | OAuth: initiate authorization flow
[**oauth_callback_api**](MarketplaceApiApi.md#oauth_callback_api) | **POST** /api/v1/marketplace/oauth/callback | OAuth: handle callback after authorization
[**trigger_sync_api**](MarketplaceApiApi.md#trigger_sync_api) | **POST** /api/v1/marketplace/connections/{connection_id}/sync | Trigger sync for a connection
[**update_connection_api**](MarketplaceApiApi.md#update_connection_api) | **PUT** /api/v1/marketplace/connections/{connection_id} | Update a connection
[**update_sync_direction_api**](MarketplaceApiApi.md#update_sync_direction_api) | **PUT** /api/v1/marketplace/connections/{connection_id}/directions | Update per-entity sync direction configuration for a connection
[**webhook_receiver_api**](MarketplaceApiApi.md#webhook_receiver_api) | **POST** /api/v1/marketplace/webhook/{platform}/{connection_id} | Webhook receiver


# **create_connection_api**
> MarketplaceConnection create_connection_api(create_connection_request => $create_connection_request)

Create a new connection (for API-key based platforms)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $create_connection_request = WWW::OpenAPIClient::Object::CreateConnectionRequest->new(); # CreateConnectionRequest | 

eval {
    my $result = $api_instance->create_connection_api(create_connection_request => $create_connection_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->create_connection_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_connection_request** | [**CreateConnectionRequest**](CreateConnectionRequest.md)|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_connection_api**
> delete_connection_api(connection_id => $connection_id)

Soft-delete a connection

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $connection_id = "connection_id_example"; # string | 

eval {
    $api_instance->delete_connection_api(connection_id => $connection_id);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->delete_connection_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connection_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_connection_api**
> MarketplaceConnection get_connection_api(connection_id => $connection_id)

Get a single connection

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $connection_id = "connection_id_example"; # string | 

eval {
    my $result = $api_instance->get_connection_api(connection_id => $connection_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->get_connection_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connection_id** | **string**|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sync_direction_api**
> get_sync_direction_api(connection_id => $connection_id)

Get current sync direction configuration for a connection

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $connection_id = "connection_id_example"; # string | 

eval {
    $api_instance->get_sync_direction_api(connection_id => $connection_id);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->get_sync_direction_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connection_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sync_logs_api**
> ARRAY[SyncLog] get_sync_logs_api(connection_id => $connection_id)

Get sync logs for a connection

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $connection_id = "connection_id_example"; # string | 

eval {
    my $result = $api_instance->get_sync_logs_api(connection_id => $connection_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->get_sync_logs_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connection_id** | **string**|  | 

### Return type

[**ARRAY[SyncLog]**](SyncLog.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_connections_api**
> ARRAY[MarketplaceConnection] list_connections_api()

List connections for the current tenant

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_connections_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->list_connections_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[MarketplaceConnection]**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_platforms_api**
> ARRAY[PlatformInfo] list_platforms_api()

List all supported platforms

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_platforms_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->list_platforms_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[PlatformInfo]**](PlatformInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_authorize_api**
> OAuthAuthorizeResponse oauth_authorize_api(o_auth_authorize_request => $o_auth_authorize_request)

OAuth: initiate authorization flow

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $o_auth_authorize_request = WWW::OpenAPIClient::Object::OAuthAuthorizeRequest->new(); # OAuthAuthorizeRequest | 

eval {
    my $result = $api_instance->oauth_authorize_api(o_auth_authorize_request => $o_auth_authorize_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->oauth_authorize_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **o_auth_authorize_request** | [**OAuthAuthorizeRequest**](OAuthAuthorizeRequest.md)|  | 

### Return type

[**OAuthAuthorizeResponse**](OAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_callback_api**
> MarketplaceConnection oauth_callback_api(o_auth_callback_request => $o_auth_callback_request)

OAuth: handle callback after authorization

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $o_auth_callback_request = WWW::OpenAPIClient::Object::OAuthCallbackRequest->new(); # OAuthCallbackRequest | 

eval {
    my $result = $api_instance->oauth_callback_api(o_auth_callback_request => $o_auth_callback_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->oauth_callback_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **o_auth_callback_request** | [**OAuthCallbackRequest**](OAuthCallbackRequest.md)|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **trigger_sync_api**
> SyncSummary trigger_sync_api(connection_id => $connection_id, sync_type => $sync_type, direction => $direction)

Trigger sync for a connection

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $connection_id = "connection_id_example"; # string | 
my $sync_type = "sync_type_example"; # string | 
my $direction = "direction_example"; # string | 

eval {
    my $result = $api_instance->trigger_sync_api(connection_id => $connection_id, sync_type => $sync_type, direction => $direction);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->trigger_sync_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connection_id** | **string**|  | 
 **sync_type** | **string**|  | [optional] 
 **direction** | **string**|  | [optional] 

### Return type

[**SyncSummary**](SyncSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_connection_api**
> MarketplaceConnection update_connection_api(connection_id => $connection_id, update_connection_request => $update_connection_request)

Update a connection

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $connection_id = "connection_id_example"; # string | 
my $update_connection_request = WWW::OpenAPIClient::Object::UpdateConnectionRequest->new(); # UpdateConnectionRequest | 

eval {
    my $result = $api_instance->update_connection_api(connection_id => $connection_id, update_connection_request => $update_connection_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->update_connection_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connection_id** | **string**|  | 
 **update_connection_request** | [**UpdateConnectionRequest**](UpdateConnectionRequest.md)|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_sync_direction_api**
> update_sync_direction_api(connection_id => $connection_id, update_sync_direction_request => $update_sync_direction_request)

Update per-entity sync direction configuration for a connection

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $connection_id = "connection_id_example"; # string | 
my $update_sync_direction_request = WWW::OpenAPIClient::Object::UpdateSyncDirectionRequest->new(); # UpdateSyncDirectionRequest | 

eval {
    $api_instance->update_sync_direction_api(connection_id => $connection_id, update_sync_direction_request => $update_sync_direction_request);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->update_sync_direction_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **connection_id** | **string**|  | 
 **update_sync_direction_request** | [**UpdateSyncDirectionRequest**](UpdateSyncDirectionRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **webhook_receiver_api**
> webhook_receiver_api(platform => $platform, connection_id => $connection_id)

Webhook receiver

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::MarketplaceApiApi;
my $api_instance = WWW::OpenAPIClient::MarketplaceApiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $platform = "platform_example"; # string | 
my $connection_id = "connection_id_example"; # string | 

eval {
    $api_instance->webhook_receiver_api(platform => $platform, connection_id => $connection_id);
};
if ($@) {
    warn "Exception when calling MarketplaceApiApi->webhook_receiver_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **string**|  | 
 **connection_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

