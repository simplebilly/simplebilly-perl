# WWW::OpenAPIClient::ShopApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::ShopApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**shop_editor_save**](ShopApi.md#shop_editor_save) | **POST** /api/v1/shop/editor | 


# **shop_editor_save**
> object shop_editor_save(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::ShopApi;
my $api_instance = WWW::OpenAPIClient::ShopApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->shop_editor_save(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling ShopApi->shop_editor_save: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

