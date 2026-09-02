# WWW::OpenAPIClient::UserManagementApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::UserManagementApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_user**](UserManagementApi.md#get_user) | **GET** /api/v1/users/{user_id} | 
[**list_users**](UserManagementApi.md#list_users) | **GET** /api/v1/users | 
[**remove_user**](UserManagementApi.md#remove_user) | **DELETE** /api/v1/users/{user_id} | 
[**update_user_permissions**](UserManagementApi.md#update_user_permissions) | **PUT** /api/v1/users/{user_id}/permissions | 
[**update_user_role**](UserManagementApi.md#update_user_role) | **PUT** /api/v1/users/{user_id}/role | 


# **get_user**
> TenantUser get_user(user_id => $user_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserManagementApi;
my $api_instance = WWW::OpenAPIClient::UserManagementApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $user_id = "user_id_example"; # string | 

eval {
    my $result = $api_instance->get_user(user_id => $user_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UserManagementApi->get_user: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**|  | 

### Return type

[**TenantUser**](TenantUser.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_users**
> ARRAY[TenantUser] list_users()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserManagementApi;
my $api_instance = WWW::OpenAPIClient::UserManagementApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_users();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UserManagementApi->list_users: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[TenantUser]**](TenantUser.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_user**
> remove_user(user_id => $user_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserManagementApi;
my $api_instance = WWW::OpenAPIClient::UserManagementApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $user_id = "user_id_example"; # string | 

eval {
    $api_instance->remove_user(user_id => $user_id);
};
if ($@) {
    warn "Exception when calling UserManagementApi->remove_user: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_user_permissions**
> update_user_permissions(user_id => $user_id, update_permissions_payload => $update_permissions_payload)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserManagementApi;
my $api_instance = WWW::OpenAPIClient::UserManagementApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $user_id = "user_id_example"; # string | 
my $update_permissions_payload = WWW::OpenAPIClient::Object::UpdatePermissionsPayload->new(); # UpdatePermissionsPayload | 

eval {
    $api_instance->update_user_permissions(user_id => $user_id, update_permissions_payload => $update_permissions_payload);
};
if ($@) {
    warn "Exception when calling UserManagementApi->update_user_permissions: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**|  | 
 **update_permissions_payload** | [**UpdatePermissionsPayload**](UpdatePermissionsPayload.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_user_role**
> update_user_role(user_id => $user_id, update_role_payload => $update_role_payload)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserManagementApi;
my $api_instance = WWW::OpenAPIClient::UserManagementApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $user_id = "user_id_example"; # string | 
my $update_role_payload = WWW::OpenAPIClient::Object::UpdateRolePayload->new(); # UpdateRolePayload | 

eval {
    $api_instance->update_user_role(user_id => $user_id, update_role_payload => $update_role_payload);
};
if ($@) {
    warn "Exception when calling UserManagementApi->update_user_role: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**|  | 
 **update_role_payload** | [**UpdateRolePayload**](UpdateRolePayload.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

