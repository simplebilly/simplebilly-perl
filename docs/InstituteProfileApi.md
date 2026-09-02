# WWW::OpenAPIClient::InstituteProfileApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::InstituteProfileApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_institute_profile**](InstituteProfileApi.md#get_institute_profile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing).
[**update_institute_profile**](InstituteProfileApi.md#update_institute_profile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert).


# **get_institute_profile**
> InstituteProfile get_institute_profile()

Current institute profile (created with defaults when missing).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InstituteProfileApi;
my $api_instance = WWW::OpenAPIClient::InstituteProfileApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_institute_profile();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InstituteProfileApi->get_institute_profile: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_institute_profile**
> InstituteProfile update_institute_profile(institute_profile_update => $institute_profile_update)

Update the institute profile (institute_type and/or kapitalmarktorientiert).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::InstituteProfileApi;
my $api_instance = WWW::OpenAPIClient::InstituteProfileApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $institute_profile_update = WWW::OpenAPIClient::Object::InstituteProfileUpdate->new(); # InstituteProfileUpdate | 

eval {
    my $result = $api_instance->update_institute_profile(institute_profile_update => $institute_profile_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling InstituteProfileApi->update_institute_profile: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **institute_profile_update** | [**InstituteProfileUpdate**](InstituteProfileUpdate.md)|  | 

### Return type

[**InstituteProfile**](InstituteProfile.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

