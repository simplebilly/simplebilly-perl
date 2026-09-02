# WWW::OpenAPIClient::SilentPartnerApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::SilentPartnerApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_silent_partner**](SilentPartnerApi.md#create_silent_partner) | **POST** /api/v1/silent-partners | 
[**delete_silent_partner**](SilentPartnerApi.md#delete_silent_partner) | **DELETE** /api/v1/silent-partners/{id} | 
[**get_silent_partner**](SilentPartnerApi.md#get_silent_partner) | **GET** /api/v1/silent-partners/{id} | 
[**get_silent_partners**](SilentPartnerApi.md#get_silent_partners) | **GET** /api/v1/silent-partners/ | 
[**update_silent_partner**](SilentPartnerApi.md#update_silent_partner) | **PUT** /api/v1/silent-partners/{id} | 


# **create_silent_partner**
> SilentPartner create_silent_partner(silent_partner_create => $silent_partner_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SilentPartnerApi;
my $api_instance = WWW::OpenAPIClient::SilentPartnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $silent_partner_create = WWW::OpenAPIClient::Object::SilentPartnerCreate->new(); # SilentPartnerCreate | 

eval {
    my $result = $api_instance->create_silent_partner(silent_partner_create => $silent_partner_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SilentPartnerApi->create_silent_partner: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **silent_partner_create** | [**SilentPartnerCreate**](SilentPartnerCreate.md)|  | 

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_silent_partner**
> delete_silent_partner(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SilentPartnerApi;
my $api_instance = WWW::OpenAPIClient::SilentPartnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_silent_partner(id => $id);
};
if ($@) {
    warn "Exception when calling SilentPartnerApi->delete_silent_partner: $@\n";
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

# **get_silent_partner**
> SilentPartner get_silent_partner(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SilentPartnerApi;
my $api_instance = WWW::OpenAPIClient::SilentPartnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_silent_partner(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SilentPartnerApi->get_silent_partner: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_silent_partners**
> ARRAY[SilentPartner] get_silent_partners(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SilentPartnerApi;
my $api_instance = WWW::OpenAPIClient::SilentPartnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_silent_partners(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SilentPartnerApi->get_silent_partners: $@\n";
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

[**ARRAY[SilentPartner]**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_silent_partner**
> SilentPartner update_silent_partner(id => $id, silent_partner_update => $silent_partner_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SilentPartnerApi;
my $api_instance = WWW::OpenAPIClient::SilentPartnerApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $silent_partner_update = WWW::OpenAPIClient::Object::SilentPartnerUpdate->new(); # SilentPartnerUpdate | 

eval {
    my $result = $api_instance->update_silent_partner(id => $id, silent_partner_update => $silent_partner_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SilentPartnerApi->update_silent_partner: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **silent_partner_update** | [**SilentPartnerUpdate**](SilentPartnerUpdate.md)|  | 

### Return type

[**SilentPartner**](SilentPartner.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

