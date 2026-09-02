# WWW::OpenAPIClient::ParticipationApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ParticipationApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_participation**](ParticipationApi.md#create_participation) | **POST** /api/v1/participations | 
[**delete_participation**](ParticipationApi.md#delete_participation) | **DELETE** /api/v1/participations/{id} | 
[**get_participation**](ParticipationApi.md#get_participation) | **GET** /api/v1/participations/{id} | 
[**get_participations**](ParticipationApi.md#get_participations) | **GET** /api/v1/participations/ | 
[**update_participation**](ParticipationApi.md#update_participation) | **PUT** /api/v1/participations/{id} | 


# **create_participation**
> Participation create_participation(participation_create => $participation_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ParticipationApi;
my $api_instance = WWW::OpenAPIClient::ParticipationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $participation_create = WWW::OpenAPIClient::Object::ParticipationCreate->new(); # ParticipationCreate | 

eval {
    my $result = $api_instance->create_participation(participation_create => $participation_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ParticipationApi->create_participation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **participation_create** | [**ParticipationCreate**](ParticipationCreate.md)|  | 

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_participation**
> delete_participation(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ParticipationApi;
my $api_instance = WWW::OpenAPIClient::ParticipationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_participation(id => $id);
};
if ($@) {
    warn "Exception when calling ParticipationApi->delete_participation: $@\n";
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

# **get_participation**
> Participation get_participation(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ParticipationApi;
my $api_instance = WWW::OpenAPIClient::ParticipationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_participation(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ParticipationApi->get_participation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_participations**
> ARRAY[Participation] get_participations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ParticipationApi;
my $api_instance = WWW::OpenAPIClient::ParticipationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_participations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ParticipationApi->get_participations: $@\n";
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

[**ARRAY[Participation]**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_participation**
> Participation update_participation(id => $id, participation_update => $participation_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ParticipationApi;
my $api_instance = WWW::OpenAPIClient::ParticipationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $participation_update = WWW::OpenAPIClient::Object::ParticipationUpdate->new(); # ParticipationUpdate | 

eval {
    my $result = $api_instance->update_participation(id => $id, participation_update => $participation_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ParticipationApi->update_participation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **participation_update** | [**ParticipationUpdate**](ParticipationUpdate.md)|  | 

### Return type

[**Participation**](Participation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

