# WWW::OpenAPIClient::TenantSettingsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::TenantSettingsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_tenant_settings**](TenantSettingsApi.md#get_tenant_settings) | **GET** /api/v1/settings/tenant | 
[**update_tenant_settings**](TenantSettingsApi.md#update_tenant_settings) | **PUT** /api/v1/settings/tenant | 


# **get_tenant_settings**
> TenantSettings get_tenant_settings()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TenantSettingsApi;
my $api_instance = WWW::OpenAPIClient::TenantSettingsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_tenant_settings();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TenantSettingsApi->get_tenant_settings: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_tenant_settings**
> TenantSettings update_tenant_settings(update_tenant_settings => $update_tenant_settings)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TenantSettingsApi;
my $api_instance = WWW::OpenAPIClient::TenantSettingsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $update_tenant_settings = WWW::OpenAPIClient::Object::UpdateTenantSettings->new(); # UpdateTenantSettings | 

eval {
    my $result = $api_instance->update_tenant_settings(update_tenant_settings => $update_tenant_settings);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TenantSettingsApi->update_tenant_settings: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_tenant_settings** | [**UpdateTenantSettings**](UpdateTenantSettings.md)|  | 

### Return type

[**TenantSettings**](TenantSettings.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

