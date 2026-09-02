# WWW::OpenAPIClient::AbsenceApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AbsenceApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_absence**](AbsenceApi.md#create_absence) | **POST** /api/v1/absences | 
[**delete_absence**](AbsenceApi.md#delete_absence) | **DELETE** /api/v1/absences/{id} | 
[**get_absence**](AbsenceApi.md#get_absence) | **GET** /api/v1/absences/{id} | 
[**get_absences**](AbsenceApi.md#get_absences) | **GET** /api/v1/absences/ | 
[**update_absence**](AbsenceApi.md#update_absence) | **PUT** /api/v1/absences/{id} | 


# **create_absence**
> Absence create_absence(absence_create => $absence_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AbsenceApi;
my $api_instance = WWW::OpenAPIClient::AbsenceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $absence_create = WWW::OpenAPIClient::Object::AbsenceCreate->new(); # AbsenceCreate | 

eval {
    my $result = $api_instance->create_absence(absence_create => $absence_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AbsenceApi->create_absence: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **absence_create** | [**AbsenceCreate**](AbsenceCreate.md)|  | 

### Return type

[**Absence**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_absence**
> delete_absence(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AbsenceApi;
my $api_instance = WWW::OpenAPIClient::AbsenceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_absence(id => $id);
};
if ($@) {
    warn "Exception when calling AbsenceApi->delete_absence: $@\n";
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

# **get_absence**
> Absence get_absence(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AbsenceApi;
my $api_instance = WWW::OpenAPIClient::AbsenceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_absence(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AbsenceApi->get_absence: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Absence**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_absences**
> ARRAY[Absence] get_absences(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AbsenceApi;
my $api_instance = WWW::OpenAPIClient::AbsenceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_absences(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AbsenceApi->get_absences: $@\n";
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

[**ARRAY[Absence]**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_absence**
> Absence update_absence(id => $id, absence_update => $absence_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AbsenceApi;
my $api_instance = WWW::OpenAPIClient::AbsenceApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $absence_update = WWW::OpenAPIClient::Object::AbsenceUpdate->new(); # AbsenceUpdate | 

eval {
    my $result = $api_instance->update_absence(id => $id, absence_update => $absence_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AbsenceApi->update_absence: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **absence_update** | [**AbsenceUpdate**](AbsenceUpdate.md)|  | 

### Return type

[**Absence**](Absence.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

