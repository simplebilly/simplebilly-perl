# WWW::OpenAPIClient::AttachmentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AttachmentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**attachment_restore**](AttachmentApi.md#attachment_restore) | **POST** /api/v1/attachments/{id}/restore | 
[**create_attachment**](AttachmentApi.md#create_attachment) | **POST** /api/v1/attachments | 
[**delete_attachment**](AttachmentApi.md#delete_attachment) | **DELETE** /api/v1/attachments/{id} | 
[**get_attachment**](AttachmentApi.md#get_attachment) | **GET** /api/v1/attachments/{id} | 
[**list_attachments**](AttachmentApi.md#list_attachments) | **GET** /api/v1/attachments/ | 
[**save_attachment_ocr_text**](AttachmentApi.md#save_attachment_ocr_text) | **PUT** /api/v1/attachments/{attachment_id}/ocr-text | Persist client-side OCR output for an attachment.


# **attachment_restore**
> Attachment attachment_restore(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentApi;
my $api_instance = WWW::OpenAPIClient::AttachmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->attachment_restore(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentApi->attachment_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_attachment**
> Attachment create_attachment(attachment_create => $attachment_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentApi;
my $api_instance = WWW::OpenAPIClient::AttachmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attachment_create = WWW::OpenAPIClient::Object::AttachmentCreate->new(); # AttachmentCreate | 

eval {
    my $result = $api_instance->create_attachment(attachment_create => $attachment_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentApi->create_attachment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachment_create** | [**AttachmentCreate**](AttachmentCreate.md)|  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_attachment**
> delete_attachment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentApi;
my $api_instance = WWW::OpenAPIClient::AttachmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_attachment(id => $id);
};
if ($@) {
    warn "Exception when calling AttachmentApi->delete_attachment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_attachment**
> Attachment get_attachment(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentApi;
my $api_instance = WWW::OpenAPIClient::AttachmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_attachment(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentApi->get_attachment: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_attachments**
> ARRAY[Attachment] list_attachments(page => $page, page_size => $page_size, contact_id => $contact_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentApi;
my $api_instance = WWW::OpenAPIClient::AttachmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $contact_id = "contact_id_example"; # string | 

eval {
    my $result = $api_instance->list_attachments(page => $page, page_size => $page_size, contact_id => $contact_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentApi->list_attachments: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **contact_id** | **string**|  | [optional] 

### Return type

[**ARRAY[Attachment]**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **save_attachment_ocr_text**
> Attachment save_attachment_ocr_text(attachment_id => $attachment_id, ocr_text_request => $ocr_text_request)

Persist client-side OCR output for an attachment.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AttachmentApi;
my $api_instance = WWW::OpenAPIClient::AttachmentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $attachment_id = "attachment_id_example"; # string | 
my $ocr_text_request = WWW::OpenAPIClient::Object::OcrTextRequest->new(); # OcrTextRequest | 

eval {
    my $result = $api_instance->save_attachment_ocr_text(attachment_id => $attachment_id, ocr_text_request => $ocr_text_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AttachmentApi->save_attachment_ocr_text: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **attachment_id** | **string**|  | 
 **ocr_text_request** | [**OcrTextRequest**](OcrTextRequest.md)|  | 

### Return type

[**Attachment**](Attachment.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

