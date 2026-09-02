# WWW::OpenAPIClient::SupportChannelApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::SupportChannelApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_channel_api**](SupportChannelApi.md#create_channel_api) | **POST** /api/v1/support/channels | 
[**delete_channel_api**](SupportChannelApi.md#delete_channel_api) | **DELETE** /api/v1/support/channels/{channel_id} | 
[**list_channels_api**](SupportChannelApi.md#list_channels_api) | **GET** /api/v1/support/channels | 
[**update_channel_api**](SupportChannelApi.md#update_channel_api) | **PUT** /api/v1/support/channels/{channel_id} | 


# **create_channel_api**
> SupportChannel create_channel_api(create_channel_dto => $create_channel_dto)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportChannelApi;
my $api_instance = WWW::OpenAPIClient::SupportChannelApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $create_channel_dto = WWW::OpenAPIClient::Object::CreateChannelDto->new(); # CreateChannelDto | 

eval {
    my $result = $api_instance->create_channel_api(create_channel_dto => $create_channel_dto);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupportChannelApi->create_channel_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_channel_dto** | [**CreateChannelDto**](CreateChannelDto.md)|  | 

### Return type

[**SupportChannel**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_channel_api**
> delete_channel_api(channel_id => $channel_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportChannelApi;
my $api_instance = WWW::OpenAPIClient::SupportChannelApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $channel_id = "channel_id_example"; # string | 

eval {
    $api_instance->delete_channel_api(channel_id => $channel_id);
};
if ($@) {
    warn "Exception when calling SupportChannelApi->delete_channel_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_channels_api**
> ARRAY[SupportChannel] list_channels_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportChannelApi;
my $api_instance = WWW::OpenAPIClient::SupportChannelApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_channels_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupportChannelApi->list_channels_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[SupportChannel]**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_channel_api**
> SupportChannel update_channel_api(channel_id => $channel_id, update_channel_dto => $update_channel_dto)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportChannelApi;
my $api_instance = WWW::OpenAPIClient::SupportChannelApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $channel_id = "channel_id_example"; # string | 
my $update_channel_dto = WWW::OpenAPIClient::Object::UpdateChannelDto->new(); # UpdateChannelDto | 

eval {
    my $result = $api_instance->update_channel_api(channel_id => $channel_id, update_channel_dto => $update_channel_dto);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupportChannelApi->update_channel_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel_id** | **string**|  | 
 **update_channel_dto** | [**UpdateChannelDto**](UpdateChannelDto.md)|  | 

### Return type

[**SupportChannel**](SupportChannel.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

