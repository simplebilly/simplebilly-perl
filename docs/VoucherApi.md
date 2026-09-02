# WWW::OpenAPIClient::VoucherApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::VoucherApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_voucher**](VoucherApi.md#create_voucher) | **POST** /api/v1/vouchers | 
[**delete_voucher**](VoucherApi.md#delete_voucher) | **DELETE** /api/v1/vouchers/{voucher_id} | 
[**get_voucher**](VoucherApi.md#get_voucher) | **GET** /api/v1/vouchers/{voucher_id} | 
[**list_vouchers**](VoucherApi.md#list_vouchers) | **GET** /api/v1/vouchers/ | 
[**update_voucher**](VoucherApi.md#update_voucher) | **PUT** /api/v1/vouchers/{voucher_id} | 
[**voucher_restore**](VoucherApi.md#voucher_restore) | **POST** /api/v1/vouchers/{voucher_id}/restore | 


# **create_voucher**
> Voucher create_voucher(voucher_create => $voucher_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::VoucherApi;
my $api_instance = WWW::OpenAPIClient::VoucherApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $voucher_create = WWW::OpenAPIClient::Object::VoucherCreate->new(); # VoucherCreate | 

eval {
    my $result = $api_instance->create_voucher(voucher_create => $voucher_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling VoucherApi->create_voucher: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voucher_create** | [**VoucherCreate**](VoucherCreate.md)|  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_voucher**
> delete_voucher(voucher_id => $voucher_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::VoucherApi;
my $api_instance = WWW::OpenAPIClient::VoucherApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $voucher_id = "voucher_id_example"; # string | 

eval {
    $api_instance->delete_voucher(voucher_id => $voucher_id);
};
if ($@) {
    warn "Exception when calling VoucherApi->delete_voucher: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voucher_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_voucher**
> Voucher get_voucher(voucher_id => $voucher_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::VoucherApi;
my $api_instance = WWW::OpenAPIClient::VoucherApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $voucher_id = "voucher_id_example"; # string | 

eval {
    my $result = $api_instance->get_voucher(voucher_id => $voucher_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling VoucherApi->get_voucher: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voucher_id** | **string**|  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_vouchers**
> ARRAY[Voucher] list_vouchers(page => $page, page_size => $page_size, voucher_type => $voucher_type, voucher_status => $voucher_status, contact_name => $contact_name, date_from => $date_from, date_to => $date_to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::VoucherApi;
my $api_instance = WWW::OpenAPIClient::VoucherApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $voucher_type = "voucher_type_example"; # string | 
my $voucher_status = "voucher_status_example"; # string | 
my $contact_name = "contact_name_example"; # string | 
my $date_from = DateTime->from_epoch(epoch => str2time('null')); # DATE | 
my $date_to = DateTime->from_epoch(epoch => str2time('null')); # DATE | 

eval {
    my $result = $api_instance->list_vouchers(page => $page, page_size => $page_size, voucher_type => $voucher_type, voucher_status => $voucher_status, contact_name => $contact_name, date_from => $date_from, date_to => $date_to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling VoucherApi->list_vouchers: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **voucher_type** | **string**|  | [optional] 
 **voucher_status** | **string**|  | [optional] 
 **contact_name** | **string**|  | [optional] 
 **date_from** | **DATE**|  | [optional] 
 **date_to** | **DATE**|  | [optional] 

### Return type

[**ARRAY[Voucher]**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_voucher**
> Voucher update_voucher(voucher_id => $voucher_id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::VoucherApi;
my $api_instance = WWW::OpenAPIClient::VoucherApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $voucher_id = "voucher_id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->update_voucher(voucher_id => $voucher_id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling VoucherApi->update_voucher: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voucher_id** | **string**|  | 
 **body** | **object**|  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **voucher_restore**
> Voucher voucher_restore(voucher_id => $voucher_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::VoucherApi;
my $api_instance = WWW::OpenAPIClient::VoucherApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $voucher_id = "voucher_id_example"; # string | 

eval {
    my $result = $api_instance->voucher_restore(voucher_id => $voucher_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling VoucherApi->voucher_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **voucher_id** | **string**|  | 

### Return type

[**Voucher**](Voucher.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

