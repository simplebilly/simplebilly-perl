# WWW::OpenAPIClient::SupportTicketApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::SupportTicketApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ticket_api**](SupportTicketApi.md#create_ticket_api) | **POST** /api/v1/support/tickets | 
[**delete_ticket_api**](SupportTicketApi.md#delete_ticket_api) | **DELETE** /api/v1/support/tickets/{ticket_id} | 
[**get_ticket_api**](SupportTicketApi.md#get_ticket_api) | **GET** /api/v1/support/tickets/{ticket_id} | 
[**list_tickets_api**](SupportTicketApi.md#list_tickets_api) | **GET** /api/v1/support/tickets | 
[**update_ticket_api**](SupportTicketApi.md#update_ticket_api) | **PUT** /api/v1/support/tickets/{ticket_id} | 


# **create_ticket_api**
> SupportTicket create_ticket_api(create_ticket_request => $create_ticket_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportTicketApi;
my $api_instance = WWW::OpenAPIClient::SupportTicketApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $create_ticket_request = WWW::OpenAPIClient::Object::CreateTicketRequest->new(); # CreateTicketRequest | 

eval {
    my $result = $api_instance->create_ticket_api(create_ticket_request => $create_ticket_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupportTicketApi->create_ticket_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_ticket_request** | [**CreateTicketRequest**](CreateTicketRequest.md)|  | 

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ticket_api**
> delete_ticket_api(ticket_id => $ticket_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportTicketApi;
my $api_instance = WWW::OpenAPIClient::SupportTicketApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ticket_id = "ticket_id_example"; # string | 

eval {
    $api_instance->delete_ticket_api(ticket_id => $ticket_id);
};
if ($@) {
    warn "Exception when calling SupportTicketApi->delete_ticket_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ticket_api**
> SupportTicket get_ticket_api(ticket_id => $ticket_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportTicketApi;
my $api_instance = WWW::OpenAPIClient::SupportTicketApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ticket_id = "ticket_id_example"; # string | 

eval {
    my $result = $api_instance->get_ticket_api(ticket_id => $ticket_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupportTicketApi->get_ticket_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  | 

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_tickets_api**
> ARRAY[SupportTicket] list_tickets_api(status => $status, priority => $priority, assigned_to => $assigned_to, channel_type => $channel_type, customer_id => $customer_id, search => $search, page => $page, page_size => $page_size)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportTicketApi;
my $api_instance = WWW::OpenAPIClient::SupportTicketApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $status = "status_example"; # string | 
my $priority = "priority_example"; # string | 
my $assigned_to = "assigned_to_example"; # string | 
my $channel_type = "channel_type_example"; # string | 
my $customer_id = "customer_id_example"; # string | 
my $search = "search_example"; # string | 
my $page = 56; # int | 
my $page_size = 56; # int | 

eval {
    my $result = $api_instance->list_tickets_api(status => $status, priority => $priority, assigned_to => $assigned_to, channel_type => $channel_type, customer_id => $customer_id, search => $search, page => $page, page_size => $page_size);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupportTicketApi->list_tickets_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **string**|  | [optional] 
 **priority** | **string**|  | [optional] 
 **assigned_to** | **string**|  | [optional] 
 **channel_type** | **string**|  | [optional] 
 **customer_id** | **string**|  | [optional] 
 **search** | **string**|  | [optional] 
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 

### Return type

[**ARRAY[SupportTicket]**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_ticket_api**
> SupportTicket update_ticket_api(ticket_id => $ticket_id, support_ticket_update => $support_ticket_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::SupportTicketApi;
my $api_instance = WWW::OpenAPIClient::SupportTicketApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ticket_id = "ticket_id_example"; # string | 
my $support_ticket_update = WWW::OpenAPIClient::Object::SupportTicketUpdate->new(); # SupportTicketUpdate | 

eval {
    my $result = $api_instance->update_ticket_api(ticket_id => $ticket_id, support_ticket_update => $support_ticket_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling SupportTicketApi->update_ticket_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ticket_id** | **string**|  | 
 **support_ticket_update** | [**SupportTicketUpdate**](SupportTicketUpdate.md)|  | 

### Return type

[**SupportTicket**](SupportTicket.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

