# WWW::OpenAPIClient::PackingApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PackingApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**complete_packing**](PackingApi.md#complete_packing) | **POST** /api/v1/packing/{order_number}/complete | Mark packing as complete and transition order to shipped
[**get_packing_queue**](PackingApi.md#get_packing_queue) | **GET** /api/v1/packing/queue | Get the packing queue - orders ready for packing
[**print_delivery_note**](PackingApi.md#print_delivery_note) | **POST** /api/v1/packing/{order_number}/print-delivery-note | Print delivery note (Lieferschein) for an order
[**print_label**](PackingApi.md#print_label) | **POST** /api/v1/packing/{order_number}/print-label | Print shipping label for an order
[**record_packing_video**](PackingApi.md#record_packing_video) | **POST** /api/v1/packing/{order_number}/record-video | Record video of packing process


# **complete_packing**
> PackingCompleteResponse complete_packing(order_number => $order_number, packing_complete_request => $packing_complete_request)

Mark packing as complete and transition order to shipped

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PackingApi;
my $api_instance = WWW::OpenAPIClient::PackingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 
my $packing_complete_request = WWW::OpenAPIClient::Object::PackingCompleteRequest->new(); # PackingCompleteRequest | 

eval {
    my $result = $api_instance->complete_packing(order_number => $order_number, packing_complete_request => $packing_complete_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PackingApi->complete_packing: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 
 **packing_complete_request** | [**PackingCompleteRequest**](PackingCompleteRequest.md)|  | 

### Return type

[**PackingCompleteResponse**](PackingCompleteResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_packing_queue**
> PackingQueue get_packing_queue(page => $page, page_size => $page_size, search => $search)

Get the packing queue - orders ready for packing

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PackingApi;
my $api_instance = WWW::OpenAPIClient::PackingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 

eval {
    my $result = $api_instance->get_packing_queue(page => $page, page_size => $page_size, search => $search);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PackingApi->get_packing_queue: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 

### Return type

[**PackingQueue**](PackingQueue.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **print_delivery_note**
> PrintDeliveryNoteResponse print_delivery_note(order_number => $order_number)

Print delivery note (Lieferschein) for an order

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PackingApi;
my $api_instance = WWW::OpenAPIClient::PackingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->print_delivery_note(order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PackingApi->print_delivery_note: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 

### Return type

[**PrintDeliveryNoteResponse**](PrintDeliveryNoteResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **print_label**
> PrintLabelResponse print_label(order_number => $order_number)

Print shipping label for an order

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PackingApi;
my $api_instance = WWW::OpenAPIClient::PackingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->print_label(order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PackingApi->print_label: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 

### Return type

[**PrintLabelResponse**](PrintLabelResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **record_packing_video**
> PackingVideoResponse record_packing_video(order_number => $order_number, body => $body)

Record video of packing process

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PackingApi;
my $api_instance = WWW::OpenAPIClient::PackingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->record_packing_video(order_number => $order_number, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PackingApi->record_packing_video: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**PackingVideoResponse**](PackingVideoResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

