# WWW::OpenAPIClient::KycRecordApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::KycRecordApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_kyc_record**](KycRecordApi.md#create_kyc_record) | **POST** /api/v1/kyc-records | 
[**delete_kyc_record**](KycRecordApi.md#delete_kyc_record) | **DELETE** /api/v1/kyc-records/{id} | 
[**get_kyc_record**](KycRecordApi.md#get_kyc_record) | **GET** /api/v1/kyc-records/{id} | 
[**get_kyc_records**](KycRecordApi.md#get_kyc_records) | **GET** /api/v1/kyc-records/ | 
[**update_kyc_record**](KycRecordApi.md#update_kyc_record) | **PUT** /api/v1/kyc-records/{id} | 


# **create_kyc_record**
> KycRecord create_kyc_record(kyc_record_create => $kyc_record_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KycRecordApi;
my $api_instance = WWW::OpenAPIClient::KycRecordApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $kyc_record_create = WWW::OpenAPIClient::Object::KycRecordCreate->new(); # KycRecordCreate | 

eval {
    my $result = $api_instance->create_kyc_record(kyc_record_create => $kyc_record_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KycRecordApi->create_kyc_record: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **kyc_record_create** | [**KycRecordCreate**](KycRecordCreate.md)|  | 

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_kyc_record**
> delete_kyc_record(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KycRecordApi;
my $api_instance = WWW::OpenAPIClient::KycRecordApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_kyc_record(id => $id);
};
if ($@) {
    warn "Exception when calling KycRecordApi->delete_kyc_record: $@\n";
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

# **get_kyc_record**
> KycRecord get_kyc_record(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KycRecordApi;
my $api_instance = WWW::OpenAPIClient::KycRecordApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_kyc_record(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KycRecordApi->get_kyc_record: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_kyc_records**
> ARRAY[KycRecord] get_kyc_records(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KycRecordApi;
my $api_instance = WWW::OpenAPIClient::KycRecordApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_kyc_records(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KycRecordApi->get_kyc_records: $@\n";
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

[**ARRAY[KycRecord]**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_kyc_record**
> KycRecord update_kyc_record(id => $id, kyc_record_update => $kyc_record_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::KycRecordApi;
my $api_instance = WWW::OpenAPIClient::KycRecordApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $kyc_record_update = WWW::OpenAPIClient::Object::KycRecordUpdate->new(); # KycRecordUpdate | 

eval {
    my $result = $api_instance->update_kyc_record(id => $id, kyc_record_update => $kyc_record_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling KycRecordApi->update_kyc_record: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **kyc_record_update** | [**KycRecordUpdate**](KycRecordUpdate.md)|  | 

### Return type

[**KycRecord**](KycRecord.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

