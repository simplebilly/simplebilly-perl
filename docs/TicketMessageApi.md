# WWW::OpenAPIClient::TicketMessageApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::TicketMessageApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_messages_api**](TicketMessageApi.md#list_messages_api) | **GET** /api/v1/support/tickets/{ticket_id}/messages | 
[**send_message_api**](TicketMessageApi.md#send_message_api) | **POST** /api/v1/support/tickets/{ticket_id}/messages | 


# **list_messages_api**
> ARRAY[TicketMessage] list_messages_api(ticket_id => $ticket_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TicketMessageApi;
my $api_instance = WWW::OpenAPIClient::TicketMessageApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ticket_id = "ticket_id_example"; # string | 

eval {
    my $result = $api_instance->list_messages_api(ticket_id => $ticket_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TicketMessageApi->list_messages_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  | 

### Return type

[**ARRAY[TicketMessage]**](TicketMessage.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_message_api**
> TicketMessage send_message_api(ticket_id => $ticket_id, send_message_dto => $send_message_dto)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TicketMessageApi;
my $api_instance = WWW::OpenAPIClient::TicketMessageApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ticket_id = "ticket_id_example"; # string | 
my $send_message_dto = WWW::OpenAPIClient::Object::SendMessageDto->new(); # SendMessageDto | 

eval {
    my $result = $api_instance->send_message_api(ticket_id => $ticket_id, send_message_dto => $send_message_dto);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TicketMessageApi->send_message_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  | 
 **send_message_dto** | [**SendMessageDto**](SendMessageDto.md)|  | 

### Return type

[**TicketMessage**](TicketMessage.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

