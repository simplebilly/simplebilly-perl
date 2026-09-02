# WWW::OpenAPIClient::DeliveryNoteApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::DeliveryNoteApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_delivery_note**](DeliveryNoteApi.md#create_delivery_note) | **POST** /api/v1/delivery-notes | 
[**delete_delivery_note**](DeliveryNoteApi.md#delete_delivery_note) | **DELETE** /api/v1/delivery-notes/{delivery_note_id} | 
[**deliverynote_restore**](DeliveryNoteApi.md#deliverynote_restore) | **POST** /api/v1/delivery-notes/{delivery_note_id}/restore | 
[**download_delivery_note_pdf**](DeliveryNoteApi.md#download_delivery_note_pdf) | **GET** /api/v1/delivery-notes/{delivery_note_id}/pdf | 
[**get_delivery_note**](DeliveryNoteApi.md#get_delivery_note) | **GET** /api/v1/delivery-notes/{delivery_note_id} | 
[**list_delivery_notes**](DeliveryNoteApi.md#list_delivery_notes) | **GET** /api/v1/delivery-notes/ | 
[**pursue_delivery_note**](DeliveryNoteApi.md#pursue_delivery_note) | **POST** /api/v1/delivery-notes/{delivery_note_id}/pursue | 


# **create_delivery_note**
> DeliveryNote create_delivery_note(delivery_note_create => $delivery_note_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryNoteApi;
my $api_instance = WWW::OpenAPIClient::DeliveryNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_note_create = WWW::OpenAPIClient::Object::DeliveryNoteCreate->new(); # DeliveryNoteCreate | 

eval {
    my $result = $api_instance->create_delivery_note(delivery_note_create => $delivery_note_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryNoteApi->create_delivery_note: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_note_create** | [**DeliveryNoteCreate**](DeliveryNoteCreate.md)|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_delivery_note**
> delete_delivery_note(delivery_note_id => $delivery_note_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryNoteApi;
my $api_instance = WWW::OpenAPIClient::DeliveryNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_note_id = "delivery_note_id_example"; # string | 

eval {
    $api_instance->delete_delivery_note(delivery_note_id => $delivery_note_id);
};
if ($@) {
    warn "Exception when calling DeliveryNoteApi->delete_delivery_note: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_note_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **deliverynote_restore**
> DeliveryNote deliverynote_restore(delivery_note_id => $delivery_note_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryNoteApi;
my $api_instance = WWW::OpenAPIClient::DeliveryNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_note_id = "delivery_note_id_example"; # string | 

eval {
    my $result = $api_instance->deliverynote_restore(delivery_note_id => $delivery_note_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryNoteApi->deliverynote_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_note_id** | **string**|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_delivery_note_pdf**
> download_delivery_note_pdf(delivery_note_id => $delivery_note_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryNoteApi;
my $api_instance = WWW::OpenAPIClient::DeliveryNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_note_id = "delivery_note_id_example"; # string | 

eval {
    $api_instance->download_delivery_note_pdf(delivery_note_id => $delivery_note_id);
};
if ($@) {
    warn "Exception when calling DeliveryNoteApi->download_delivery_note_pdf: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_note_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_delivery_note**
> DeliveryNote get_delivery_note(delivery_note_id => $delivery_note_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryNoteApi;
my $api_instance = WWW::OpenAPIClient::DeliveryNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_note_id = "delivery_note_id_example"; # string | 

eval {
    my $result = $api_instance->get_delivery_note(delivery_note_id => $delivery_note_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryNoteApi->get_delivery_note: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_note_id** | **string**|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_delivery_notes**
> ARRAY[DeliveryNote] list_delivery_notes(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryNoteApi;
my $api_instance = WWW::OpenAPIClient::DeliveryNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->list_delivery_notes(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryNoteApi->list_delivery_notes: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **include_deleted** | **boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**ARRAY[DeliveryNote]**](DeliveryNote.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pursue_delivery_note**
> Invoice pursue_delivery_note(delivery_note_id => $delivery_note_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::DeliveryNoteApi;
my $api_instance = WWW::OpenAPIClient::DeliveryNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $delivery_note_id = "delivery_note_id_example"; # string | 

eval {
    my $result = $api_instance->pursue_delivery_note(delivery_note_id => $delivery_note_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling DeliveryNoteApi->pursue_delivery_note: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **delivery_note_id** | **string**|  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

