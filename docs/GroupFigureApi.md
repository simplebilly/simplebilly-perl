# WWW::OpenAPIClient::GroupFigureApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GroupFigureApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_group_figure**](GroupFigureApi.md#create_group_figure) | **POST** /api/v1/group-figures | 
[**delete_group_figure**](GroupFigureApi.md#delete_group_figure) | **DELETE** /api/v1/group-figures/{year} | 
[**get_group_figure**](GroupFigureApi.md#get_group_figure) | **GET** /api/v1/group-figures/{year} | 
[**get_group_figures**](GroupFigureApi.md#get_group_figures) | **GET** /api/v1/group-figures/ | 
[**update_group_figure**](GroupFigureApi.md#update_group_figure) | **PUT** /api/v1/group-figures/{year} | 


# **create_group_figure**
> GroupFigure create_group_figure(group_figure_create => $group_figure_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GroupFigureApi;
my $api_instance = WWW::OpenAPIClient::GroupFigureApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $group_figure_create = WWW::OpenAPIClient::Object::GroupFigureCreate->new(); # GroupFigureCreate | 

eval {
    my $result = $api_instance->create_group_figure(group_figure_create => $group_figure_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GroupFigureApi->create_group_figure: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **group_figure_create** | [**GroupFigureCreate**](GroupFigureCreate.md)|  | 

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_group_figure**
> delete_group_figure(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GroupFigureApi;
my $api_instance = WWW::OpenAPIClient::GroupFigureApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    $api_instance->delete_group_figure(year => $year);
};
if ($@) {
    warn "Exception when calling GroupFigureApi->delete_group_figure: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_group_figure**
> GroupFigure get_group_figure(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GroupFigureApi;
my $api_instance = WWW::OpenAPIClient::GroupFigureApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->get_group_figure(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GroupFigureApi->get_group_figure: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_group_figures**
> ARRAY[GroupFigure] get_group_figures(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GroupFigureApi;
my $api_instance = WWW::OpenAPIClient::GroupFigureApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_group_figures(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GroupFigureApi->get_group_figures: $@\n";
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

[**ARRAY[GroupFigure]**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_group_figure**
> GroupFigure update_group_figure(year => $year, group_figure_update => $group_figure_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GroupFigureApi;
my $api_instance = WWW::OpenAPIClient::GroupFigureApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $group_figure_update = WWW::OpenAPIClient::Object::GroupFigureUpdate->new(); # GroupFigureUpdate | 

eval {
    my $result = $api_instance->update_group_figure(year => $year, group_figure_update => $group_figure_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GroupFigureApi->update_group_figure: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 
 **group_figure_update** | [**GroupFigureUpdate**](GroupFigureUpdate.md)|  | 

### Return type

[**GroupFigure**](GroupFigure.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

