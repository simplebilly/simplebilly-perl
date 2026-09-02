# WWW::OpenAPIClient::OnlineshopApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::OnlineshopApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_smtp_config_api**](OnlineshopApi.md#get_smtp_config_api) | **GET** /api/v1/settings/smtp | 
[**save_smtp_config_api**](OnlineshopApi.md#save_smtp_config_api) | **PUT** /api/v1/settings/smtp | 


# **get_smtp_config_api**
> SmtpConfig get_smtp_config_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OnlineshopApi;
my $api_instance = WWW::OpenAPIClient::OnlineshopApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_smtp_config_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OnlineshopApi->get_smtp_config_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**SmtpConfig**](SmtpConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **save_smtp_config_api**
> SmtpConfig save_smtp_config_api(smtp_config => $smtp_config)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::OnlineshopApi;
my $api_instance = WWW::OpenAPIClient::OnlineshopApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $smtp_config = WWW::OpenAPIClient::Object::SmtpConfig->new(); # SmtpConfig | 

eval {
    my $result = $api_instance->save_smtp_config_api(smtp_config => $smtp_config);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling OnlineshopApi->save_smtp_config_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **smtp_config** | [**SmtpConfig**](SmtpConfig.md)|  | [optional] 

### Return type

[**SmtpConfig**](SmtpConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

