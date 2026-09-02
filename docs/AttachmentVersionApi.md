# WWW::OpenAPIClient::AttachmentVersionApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AttachmentVersionApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_attachment_version**](AttachmentVersionApi.md#create_attachment_version) | **POST** /api/v1/attachments/{attachment_id}/versions | 
[**list_attachment_versions**](AttachmentVersionApi.md#list_attachment_versions) | **GET** /api/v1/attachments/{attachment_id}/versions | 
[**restore_attachment_version**](AttachmentVersionApi.md#restore_attachment_version) | **POST** /api/v1/attachments/{attachment_id}/versions/{version_id}/restore | 


# **create_attachment_version**
> AttachmentVersion create_attachment_version(attachment_id => $attachment_id, new_version_request => $new_version_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentVersionApi;
my $api_instance = WWW::OpenAPIClient::AttachmentVersionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attachment_id = "attachment_id_example"; # string | 
my $new_version_request = WWW::OpenAPIClient::Object::NewVersionRequest->new(); # NewVersionRequest | 

eval {
    my $result = $api_instance->create_attachment_version(attachment_id => $attachment_id, new_version_request => $new_version_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentVersionApi->create_attachment_version: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachment_id** | **string**|  | 
 **new_version_request** | [**NewVersionRequest**](NewVersionRequest.md)|  | 

### Return type

[**AttachmentVersion**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_attachment_versions**
> ARRAY[AttachmentVersion] list_attachment_versions(attachment_id => $attachment_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentVersionApi;
my $api_instance = WWW::OpenAPIClient::AttachmentVersionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attachment_id = "attachment_id_example"; # string | 

eval {
    my $result = $api_instance->list_attachment_versions(attachment_id => $attachment_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentVersionApi->list_attachment_versions: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachment_id** | **string**|  | 

### Return type

[**ARRAY[AttachmentVersion]**](AttachmentVersion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore_attachment_version**
> Attachment restore_attachment_version(attachment_id => $attachment_id, version_id => $version_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentVersionApi;
my $api_instance = WWW::OpenAPIClient::AttachmentVersionApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attachment_id = "attachment_id_example"; # string | 
my $version_id = "version_id_example"; # string | 

eval {
    my $result = $api_instance->restore_attachment_version(attachment_id => $attachment_id, version_id => $version_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentVersionApi->restore_attachment_version: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachment_id** | **string**|  | 
 **version_id** | **string**|  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

