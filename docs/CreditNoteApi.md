# WWW::OpenAPIClient::CreditNoteApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::CreditNoteApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_credit_note**](CreditNoteApi.md#create_credit_note) | **POST** /api/v1/credit-notes | 
[**download_credit_note_pdf**](CreditNoteApi.md#download_credit_note_pdf) | **GET** /api/v1/credit-notes/{credit_note_id}/pdf | 
[**get_credit_note**](CreditNoteApi.md#get_credit_note) | **GET** /api/v1/credit-notes/{credit_note_id} | 
[**list_credit_notes**](CreditNoteApi.md#list_credit_notes) | **GET** /api/v1/credit-notes/ | 


# **create_credit_note**
> Invoice create_credit_note(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CreditNoteApi;
my $api_instance = WWW::OpenAPIClient::CreditNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->create_credit_note(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CreditNoteApi->create_credit_note: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_credit_note_pdf**
> download_credit_note_pdf(credit_note_id => $credit_note_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CreditNoteApi;
my $api_instance = WWW::OpenAPIClient::CreditNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $credit_note_id = "credit_note_id_example"; # string | 

eval {
    $api_instance->download_credit_note_pdf(credit_note_id => $credit_note_id);
};
if ($@) {
    warn "Exception when calling CreditNoteApi->download_credit_note_pdf: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **credit_note_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_credit_note**
> Invoice get_credit_note(credit_note_id => $credit_note_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CreditNoteApi;
my $api_instance = WWW::OpenAPIClient::CreditNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $credit_note_id = "credit_note_id_example"; # string | 

eval {
    my $result = $api_instance->get_credit_note(credit_note_id => $credit_note_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CreditNoteApi->get_credit_note: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **credit_note_id** | **string**|  | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_credit_notes**
> ARRAY[Invoice] list_credit_notes(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CreditNoteApi;
my $api_instance = WWW::OpenAPIClient::CreditNoteApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->list_credit_notes(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CreditNoteApi->list_credit_notes: $@\n";
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

[**ARRAY[Invoice]**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

