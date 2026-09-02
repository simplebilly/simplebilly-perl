# WWW::OpenAPIClient::AuthApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AuthApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_invite**](AuthApi.md#accept_invite) | **POST** /auth/accept-invite | Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
[**forgot_password**](AuthApi.md#forgot_password) | **POST** /auth/forgot-password | Send a password reset email to the user
[**login**](AuthApi.md#login) | **POST** /auth/login | Authenticate a user with email + password (optional TOTP)
[**logout**](AuthApi.md#logout) | **POST** /auth/logout | Log out the current user (kills the assay session)
[**magic_link_login**](AuthApi.md#magic_link_login) | **POST** /auth/magic-link | Request a magic link login (sends an email with a one-time link)
[**magic_link_verify**](AuthApi.md#magic_link_verify) | **POST** /auth/magic-link/verify | Verify a magic link token and log the user in
[**register**](AuthApi.md#register) | **POST** /auth/register | Register a new user account
[**reset_password**](AuthApi.md#reset_password) | **POST** /auth/reset-password | Reset the user&#39;s password using a reset token
[**totp_enable**](AuthApi.md#totp_enable) | **POST** /auth/totp/enable | Enable TOTP two-factor authentication by verifying a code
[**totp_setup**](AuthApi.md#totp_setup) | **GET** /auth/totp/setup | Set up TOTP two-factor authentication (generates secret + backup codes)
[**verify_email**](AuthApi.md#verify_email) | **POST** /auth/verify-email | Verify a user&#39;s email address using a verification token


# **accept_invite**
> accept_invite(accept_invite_request => $accept_invite_request)

Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $accept_invite_request = WWW::OpenAPIClient::Object::AcceptInviteRequest->new(); # AcceptInviteRequest | 

eval {
    $api_instance->accept_invite(accept_invite_request => $accept_invite_request);
};
if ($@) {
    warn "Exception when calling AuthApi->accept_invite: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **accept_invite_request** | [**AcceptInviteRequest**](AcceptInviteRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **forgot_password**
> forgot_password(forgot_password_request => $forgot_password_request)

Send a password reset email to the user

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $forgot_password_request = WWW::OpenAPIClient::Object::ForgotPasswordRequest->new(); # ForgotPasswordRequest | 

eval {
    $api_instance->forgot_password(forgot_password_request => $forgot_password_request);
};
if ($@) {
    warn "Exception when calling AuthApi->forgot_password: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **forgot_password_request** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **login**
> AuthResponse login(login_request => $login_request)

Authenticate a user with email + password (optional TOTP)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $login_request = WWW::OpenAPIClient::Object::LoginRequest->new(); # LoginRequest | 

eval {
    my $result = $api_instance->login(login_request => $login_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AuthApi->login: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **login_request** | [**LoginRequest**](LoginRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **logout**
> logout()

Log out the current user (kills the assay session)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    $api_instance->logout();
};
if ($@) {
    warn "Exception when calling AuthApi->logout: $@\n";
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

# **magic_link_login**
> magic_link_login(magic_link_request => $magic_link_request)

Request a magic link login (sends an email with a one-time link)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $magic_link_request = WWW::OpenAPIClient::Object::MagicLinkRequest->new(); # MagicLinkRequest | 

eval {
    $api_instance->magic_link_login(magic_link_request => $magic_link_request);
};
if ($@) {
    warn "Exception when calling AuthApi->magic_link_login: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **magic_link_request** | [**MagicLinkRequest**](MagicLinkRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **magic_link_verify**
> AuthResponse magic_link_verify(magic_link_verify_request => $magic_link_verify_request)

Verify a magic link token and log the user in

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $magic_link_verify_request = WWW::OpenAPIClient::Object::MagicLinkVerifyRequest->new(); # MagicLinkVerifyRequest | 

eval {
    my $result = $api_instance->magic_link_verify(magic_link_verify_request => $magic_link_verify_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AuthApi->magic_link_verify: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **magic_link_verify_request** | [**MagicLinkVerifyRequest**](MagicLinkVerifyRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register**
> AuthResponse register(register_request => $register_request)

Register a new user account

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $register_request = WWW::OpenAPIClient::Object::RegisterRequest->new(); # RegisterRequest | 

eval {
    my $result = $api_instance->register(register_request => $register_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AuthApi->register: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **register_request** | [**RegisterRequest**](RegisterRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_password**
> reset_password(reset_password_request => $reset_password_request)

Reset the user's password using a reset token

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $reset_password_request = WWW::OpenAPIClient::Object::ResetPasswordRequest->new(); # ResetPasswordRequest | 

eval {
    $api_instance->reset_password(reset_password_request => $reset_password_request);
};
if ($@) {
    warn "Exception when calling AuthApi->reset_password: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **reset_password_request** | [**ResetPasswordRequest**](ResetPasswordRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **totp_enable**
> totp_enable(totp_enable_request => $totp_enable_request)

Enable TOTP two-factor authentication by verifying a code

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $totp_enable_request = WWW::OpenAPIClient::Object::TotpEnableRequest->new(); # TotpEnableRequest | 

eval {
    $api_instance->totp_enable(totp_enable_request => $totp_enable_request);
};
if ($@) {
    warn "Exception when calling AuthApi->totp_enable: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **totp_enable_request** | [**TotpEnableRequest**](TotpEnableRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **totp_setup**
> TotpSetupResponse totp_setup()

Set up TOTP two-factor authentication (generates secret + backup codes)

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->totp_setup();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AuthApi->totp_setup: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TotpSetupResponse**](TotpSetupResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **verify_email**
> verify_email(verify_email_request => $verify_email_request)

Verify a user's email address using a verification token

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AuthApi;
my $api_instance = WWW::OpenAPIClient::AuthApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $verify_email_request = WWW::OpenAPIClient::Object::VerifyEmailRequest->new(); # VerifyEmailRequest | 

eval {
    $api_instance->verify_email(verify_email_request => $verify_email_request);
};
if ($@) {
    warn "Exception when calling AuthApi->verify_email: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **verify_email_request** | [**VerifyEmailRequest**](VerifyEmailRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

