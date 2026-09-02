# WWW::OpenAPIClient::UserApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::UserApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**change_password**](UserApi.md#change_password) | **POST** /user/change-password | Change the current user&#39;s password (requires the current password).
[**create_team**](UserApi.md#create_team) | **POST** /user/teams | Create a new team within the current tenant
[**generate_api_key**](UserApi.md#generate_api_key) | **POST** /user/api-key | Generate a new API key for the current user
[**invite_user**](UserApi.md#invite_user) | **POST** /user/invite | Invite a user to the current tenant/organization
[**list_teams**](UserApi.md#list_teams) | **GET** /user/teams | List all teams in the current tenant
[**remove_user_from_org**](UserApi.md#remove_user_from_org) | **DELETE** /user/remove | Remove a user from the current organization
[**update_profile**](UserApi.md#update_profile) | **PUT** /user/profile | Update the current user&#39;s profile
[**user_profile**](UserApi.md#user_profile) | **GET** /user/profile | Get the current user&#39;s profile
[**user_tenants**](UserApi.md#user_tenants) | **GET** /user/tenants | List all tenants (organizations) the current user belongs to


# **change_password**
> change_password(change_password_request => $change_password_request)

Change the current user's password (requires the current password).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $change_password_request = WWW::OpenAPIClient::Object::ChangePasswordRequest->new(); # ChangePasswordRequest | 

eval {
    $api_instance->change_password(change_password_request => $change_password_request);
};
if ($@) {
    warn "Exception when calling UserApi->change_password: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **change_password_request** | [**ChangePasswordRequest**](ChangePasswordRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_team**
> ApiResponseTeam create_team(team_create => $team_create)

Create a new team within the current tenant

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $team_create = WWW::OpenAPIClient::Object::TeamCreate->new(); # TeamCreate | 

eval {
    my $result = $api_instance->create_team(team_create => $team_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UserApi->create_team: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **team_create** | [**TeamCreate**](TeamCreate.md)|  | 

### Return type

[**ApiResponseTeam**](ApiResponseTeam.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **generate_api_key**
> ApiResponseString generate_api_key()

Generate a new API key for the current user

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->generate_api_key();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UserApi->generate_api_key: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseString**](ApiResponseString.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **invite_user**
> invite_user(invite_request => $invite_request)

Invite a user to the current tenant/organization

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $invite_request = WWW::OpenAPIClient::Object::InviteRequest->new(); # InviteRequest | 

eval {
    $api_instance->invite_user(invite_request => $invite_request);
};
if ($@) {
    warn "Exception when calling UserApi->invite_user: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **invite_request** | [**InviteRequest**](InviteRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_teams**
> ApiResponseVecTeam list_teams()

List all teams in the current tenant

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_teams();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UserApi->list_teams: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseVecTeam**](ApiResponseVecTeam.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_user_from_org**
> remove_user_from_org(remove_user_request => $remove_user_request)

Remove a user from the current organization

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $remove_user_request = WWW::OpenAPIClient::Object::RemoveUserRequest->new(); # RemoveUserRequest | 

eval {
    $api_instance->remove_user_from_org(remove_user_request => $remove_user_request);
};
if ($@) {
    warn "Exception when calling UserApi->remove_user_from_org: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **remove_user_request** | [**RemoveUserRequest**](RemoveUserRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_profile**
> update_profile(update_profile_request => $update_profile_request)

Update the current user's profile

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $update_profile_request = WWW::OpenAPIClient::Object::UpdateProfileRequest->new(); # UpdateProfileRequest | 

eval {
    $api_instance->update_profile(update_profile_request => $update_profile_request);
};
if ($@) {
    warn "Exception when calling UserApi->update_profile: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **update_profile_request** | [**UpdateProfileRequest**](UpdateProfileRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **user_profile**
> ApiResponseUserProfile user_profile()

Get the current user's profile

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->user_profile();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UserApi->user_profile: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseUserProfile**](ApiResponseUserProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **user_tenants**
> ApiResponseVecUserTenantInfo user_tenants()

List all tenants (organizations) the current user belongs to

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::UserApi;
my $api_instance = WWW::OpenAPIClient::UserApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->user_tenants();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling UserApi->user_tenants: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseVecUserTenantInfo**](ApiResponseVecUserTenantInfo.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

