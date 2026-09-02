# WWW::OpenAPIClient::QuotationApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::QuotationApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_quotation**](QuotationApi.md#create_quotation) | **POST** /api/v1/quotations | 
[**delete_quotation**](QuotationApi.md#delete_quotation) | **DELETE** /api/v1/quotations/{quotation_id} | 
[**download_quotation_pdf**](QuotationApi.md#download_quotation_pdf) | **GET** /api/v1/quotations/{quotation_id}/pdf | 
[**get_quotation**](QuotationApi.md#get_quotation) | **GET** /api/v1/quotations/{quotation_id} | 
[**list_quotations**](QuotationApi.md#list_quotations) | **GET** /api/v1/quotations/ | 
[**pursue_quotation**](QuotationApi.md#pursue_quotation) | **POST** /api/v1/quotations/{quotation_id}/pursue | 
[**quotation_restore**](QuotationApi.md#quotation_restore) | **POST** /api/v1/quotations/{quotation_id}/restore | 
[**update_quotation**](QuotationApi.md#update_quotation) | **PUT** /api/v1/quotations/{quotation_id} | 


# **create_quotation**
> Quotation create_quotation(quotation_create => $quotation_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quotation_create = WWW::OpenAPIClient::Object::QuotationCreate->new(); # QuotationCreate | 

eval {
    my $result = $api_instance->create_quotation(quotation_create => $quotation_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling QuotationApi->create_quotation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quotation_create** | [**QuotationCreate**](QuotationCreate.md)|  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_quotation**
> delete_quotation(quotation_id => $quotation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quotation_id = "quotation_id_example"; # string | 

eval {
    $api_instance->delete_quotation(quotation_id => $quotation_id);
};
if ($@) {
    warn "Exception when calling QuotationApi->delete_quotation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quotation_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **download_quotation_pdf**
> download_quotation_pdf(quotation_id => $quotation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quotation_id = "quotation_id_example"; # string | 

eval {
    $api_instance->download_quotation_pdf(quotation_id => $quotation_id);
};
if ($@) {
    warn "Exception when calling QuotationApi->download_quotation_pdf: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quotation_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_quotation**
> Quotation get_quotation(quotation_id => $quotation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quotation_id = "quotation_id_example"; # string | 

eval {
    my $result = $api_instance->get_quotation(quotation_id => $quotation_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling QuotationApi->get_quotation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quotation_id** | **string**|  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_quotations**
> ARRAY[Quotation] list_quotations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->list_quotations(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling QuotationApi->list_quotations: $@\n";
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

[**ARRAY[Quotation]**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pursue_quotation**
> OrderConfirmation pursue_quotation(quotation_id => $quotation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quotation_id = "quotation_id_example"; # string | 

eval {
    my $result = $api_instance->pursue_quotation(quotation_id => $quotation_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling QuotationApi->pursue_quotation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quotation_id** | **string**|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **quotation_restore**
> Quotation quotation_restore(quotation_id => $quotation_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quotation_id = "quotation_id_example"; # string | 

eval {
    my $result = $api_instance->quotation_restore(quotation_id => $quotation_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling QuotationApi->quotation_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quotation_id** | **string**|  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_quotation**
> Quotation update_quotation(quotation_id => $quotation_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::QuotationApi;
my $api_instance = WWW::OpenAPIClient::QuotationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $quotation_id = "quotation_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_quotation(quotation_id => $quotation_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling QuotationApi->update_quotation: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **quotation_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Quotation**](Quotation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

