# WWW::OpenAPIClient::RfqApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::RfqApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**convert_rfq**](RfqApi.md#convert_rfq) | **POST** /api/v1/rfqs/{rfq_id}/convert | Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as &#x60;converted&#x60;.
[**create_rfq**](RfqApi.md#create_rfq) | **POST** /api/v1/rfqs | 
[**delete_rfq**](RfqApi.md#delete_rfq) | **DELETE** /api/v1/rfqs/{rfq_id} | 
[**get_rfq**](RfqApi.md#get_rfq) | **GET** /api/v1/rfqs/{rfq_id} | 
[**list_rfqs**](RfqApi.md#list_rfqs) | **GET** /api/v1/rfqs/ | 
[**update_rfq**](RfqApi.md#update_rfq) | **PUT** /api/v1/rfqs/{rfq_id} | 
[**update_rfq_status**](RfqApi.md#update_rfq_status) | **PUT** /api/v1/rfqs/{rfq_id}/status | 


# **convert_rfq**
> object convert_rfq(rfq_id => $rfq_id)

Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RfqApi;
my $api_instance = WWW::OpenAPIClient::RfqApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rfq_id = "rfq_id_example"; # string | 

eval {
    my $result = $api_instance->convert_rfq(rfq_id => $rfq_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RfqApi->convert_rfq: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rfq_id** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_rfq**
> Rfq create_rfq(rfq => $rfq)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RfqApi;
my $api_instance = WWW::OpenAPIClient::RfqApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rfq = WWW::OpenAPIClient::Object::Rfq->new(); # Rfq | 

eval {
    my $result = $api_instance->create_rfq(rfq => $rfq);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RfqApi->create_rfq: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rfq** | [**Rfq**](Rfq.md)|  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_rfq**
> delete_rfq(rfq_id => $rfq_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RfqApi;
my $api_instance = WWW::OpenAPIClient::RfqApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rfq_id = "rfq_id_example"; # string | 

eval {
    $api_instance->delete_rfq(rfq_id => $rfq_id);
};
if ($@) {
    warn "Exception when calling RfqApi->delete_rfq: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rfq_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_rfq**
> Rfq get_rfq(rfq_id => $rfq_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RfqApi;
my $api_instance = WWW::OpenAPIClient::RfqApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rfq_id = "rfq_id_example"; # string | 

eval {
    my $result = $api_instance->get_rfq(rfq_id => $rfq_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RfqApi->get_rfq: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rfq_id** | **string**|  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_rfqs**
> ARRAY[Rfq] list_rfqs(page => $page, page_size => $page_size, status => $status, supplier_name => $supplier_name)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RfqApi;
my $api_instance = WWW::OpenAPIClient::RfqApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $status = "status_example"; # string | 
my $supplier_name = "supplier_name_example"; # string | 

eval {
    my $result = $api_instance->list_rfqs(page => $page, page_size => $page_size, status => $status, supplier_name => $supplier_name);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RfqApi->list_rfqs: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 
 **supplier_name** | **string**|  | [optional] 

### Return type

[**ARRAY[Rfq]**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_rfq**
> Rfq update_rfq(rfq_id => $rfq_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RfqApi;
my $api_instance = WWW::OpenAPIClient::RfqApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rfq_id = "rfq_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_rfq(rfq_id => $rfq_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RfqApi->update_rfq: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rfq_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_rfq_status**
> Rfq update_rfq_status(rfq_id => $rfq_id, rfq_status_update => $rfq_status_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::RfqApi;
my $api_instance = WWW::OpenAPIClient::RfqApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $rfq_id = "rfq_id_example"; # string | 
my $rfq_status_update = WWW::OpenAPIClient::Object::RfqStatusUpdate->new(); # RfqStatusUpdate | 

eval {
    my $result = $api_instance->update_rfq_status(rfq_id => $rfq_id, rfq_status_update => $rfq_status_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling RfqApi->update_rfq_status: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **rfq_id** | **string**|  | 
 **rfq_status_update** | [**RfqStatusUpdate**](RfqStatusUpdate.md)|  | 

### Return type

[**Rfq**](Rfq.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

