# WWW::OpenAPIClient::ContactApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ContactApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**contact_schema**](ContactApi.md#contact_schema) | **GET** /api/v1/contacts/schema | Serve JSON Schema for client-side validation
[**contact_timeline**](ContactApi.md#contact_timeline) | **GET** /api/v1/contacts/{contact_id}/timeline | Get the full per-contact timeline (Xentral §4.6/4.7).
[**create_contact**](ContactApi.md#create_contact) | **POST** /api/v1/contacts | Create contact
[**delete_contact**](ContactApi.md#delete_contact) | **DELETE** /api/v1/contacts/{contact_id} | Soft-delete contact
[**get_contact**](ContactApi.md#get_contact) | **GET** /api/v1/contacts/{contact_id} | Get single contact
[**list_contacts**](ContactApi.md#list_contacts) | **GET** /api/v1/contacts | List contacts with search, type filter, and pagination
[**sales_volume**](ContactApi.md#sales_volume) | **GET** /api/v1/contacts/sales-volume | Sales volume per contact
[**update_contact**](ContactApi.md#update_contact) | **PUT** /api/v1/contacts/{contact_id} | Update contact


# **contact_schema**
> object contact_schema()

Serve JSON Schema for client-side validation

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->contact_schema();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ContactApi->contact_schema: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **contact_timeline**
> ContactTimelineResponse contact_timeline(contact_id => $contact_id)

Get the full per-contact timeline (Xentral §4.6/4.7).

Aggregates communications, quotations, orders, invoices and uploaded documents for a contact, merged into a single reverse-chronological feed.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $contact_id = "contact_id_example"; # string | 

eval {
    my $result = $api_instance->contact_timeline(contact_id => $contact_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ContactApi->contact_timeline: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_id** | **string**|  | 

### Return type

[**ContactTimelineResponse**](ContactTimelineResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_contact**
> Contact create_contact(body => $body)

Create contact

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->create_contact(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ContactApi->create_contact: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_contact**
> delete_contact(contact_id => $contact_id)

Soft-delete contact

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $contact_id = "contact_id_example"; # string | 

eval {
    $api_instance->delete_contact(contact_id => $contact_id);
};
if ($@) {
    warn "Exception when calling ContactApi->delete_contact: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_contact**
> Contact get_contact(contact_id => $contact_id)

Get single contact

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $contact_id = "contact_id_example"; # string | 

eval {
    my $result = $api_instance->get_contact(contact_id => $contact_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ContactApi->get_contact: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_id** | **string**|  | 

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_contacts**
> ARRAY[Contact] list_contacts(page => $page, page_size => $page_size, search => $search, contact_type => $contact_type, tag => $tag)

List contacts with search, type filter, and pagination

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $contact_type = "contact_type_example"; # string | 
my $tag = "tag_example"; # string | 

eval {
    my $result = $api_instance->list_contacts(page => $page, page_size => $page_size, search => $search, contact_type => $contact_type, tag => $tag);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ContactApi->list_contacts: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **contact_type** | **string**|  | [optional] 
 **tag** | **string**|  | [optional] 

### Return type

[**ARRAY[Contact]**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sales_volume**
> SalesVolumeReport sales_volume(page => $page, page_size => $page_size, search => $search, contact_type => $contact_type, tag => $tag)

Sales volume per contact

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $contact_type = "contact_type_example"; # string | 
my $tag = "tag_example"; # string | 

eval {
    my $result = $api_instance->sales_volume(page => $page, page_size => $page_size, search => $search, contact_type => $contact_type, tag => $tag);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ContactApi->sales_volume: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **contact_type** | **string**|  | [optional] 
 **tag** | **string**|  | [optional] 

### Return type

[**SalesVolumeReport**](SalesVolumeReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_contact**
> Contact update_contact(contact_id => $contact_id, body => $body)

Update contact

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ContactApi;
my $api_instance = WWW::OpenAPIClient::ContactApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $contact_id = "contact_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_contact(contact_id => $contact_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ContactApi->update_contact: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Contact**](Contact.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

