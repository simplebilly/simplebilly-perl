# WWW::OpenAPIClient::CustomerCommunicationApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::CustomerCommunicationApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_communication**](CustomerCommunicationApi.md#create_communication) | **POST** /api/v1/communications | 
[**customercommunication_restore**](CustomerCommunicationApi.md#customercommunication_restore) | **POST** /api/v1/communications/{communication_id}/restore | 
[**delete_communication**](CustomerCommunicationApi.md#delete_communication) | **DELETE** /api/v1/communications/{communication_id} | 
[**get_communication**](CustomerCommunicationApi.md#get_communication) | **GET** /api/v1/communications/{communication_id} | 
[**get_contact_history**](CustomerCommunicationApi.md#get_contact_history) | **GET** /api/v1/contacts/{contact_id}/communications | 
[**list_communications**](CustomerCommunicationApi.md#list_communications) | **GET** /api/v1/communications/ | 
[**update_communication**](CustomerCommunicationApi.md#update_communication) | **PUT** /api/v1/communications/{communication_id} | 


# **create_communication**
> CustomerCommunication create_communication(customer_communication_create => $customer_communication_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerCommunicationApi;
my $api_instance = WWW::OpenAPIClient::CustomerCommunicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_communication_create = WWW::OpenAPIClient::Object::CustomerCommunicationCreate->new(); # CustomerCommunicationCreate | 

eval {
    my $result = $api_instance->create_communication(customer_communication_create => $customer_communication_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerCommunicationApi->create_communication: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_communication_create** | [**CustomerCommunicationCreate**](CustomerCommunicationCreate.md)|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **customercommunication_restore**
> CustomerCommunication customercommunication_restore(communication_id => $communication_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerCommunicationApi;
my $api_instance = WWW::OpenAPIClient::CustomerCommunicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $communication_id = "communication_id_example"; # string | 

eval {
    my $result = $api_instance->customercommunication_restore(communication_id => $communication_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerCommunicationApi->customercommunication_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communication_id** | **string**|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_communication**
> delete_communication(communication_id => $communication_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerCommunicationApi;
my $api_instance = WWW::OpenAPIClient::CustomerCommunicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $communication_id = "communication_id_example"; # string | 

eval {
    $api_instance->delete_communication(communication_id => $communication_id);
};
if ($@) {
    warn "Exception when calling CustomerCommunicationApi->delete_communication: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communication_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_communication**
> CustomerCommunication get_communication(communication_id => $communication_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerCommunicationApi;
my $api_instance = WWW::OpenAPIClient::CustomerCommunicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $communication_id = "communication_id_example"; # string | 

eval {
    my $result = $api_instance->get_communication(communication_id => $communication_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerCommunicationApi->get_communication: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communication_id** | **string**|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_contact_history**
> ContactHistoryResponse get_contact_history(contact_id => $contact_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerCommunicationApi;
my $api_instance = WWW::OpenAPIClient::CustomerCommunicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $contact_id = "contact_id_example"; # string | 

eval {
    my $result = $api_instance->get_contact_history(contact_id => $contact_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerCommunicationApi->get_contact_history: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_id** | **string**|  | 

### Return type

[**ContactHistoryResponse**](ContactHistoryResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_communications**
> ARRAY[CustomerCommunication] list_communications(page => $page, page_size => $page_size, contact_id => $contact_id, channel => $channel, direction => $direction, from => $from, to => $to)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerCommunicationApi;
my $api_instance = WWW::OpenAPIClient::CustomerCommunicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 56; # int | 
my $page_size = 56; # int | 
my $contact_id = "contact_id_example"; # string | Filter history to a single contact.
my $channel = new WWW::OpenAPIClient.CommunicationChannel(); # CommunicationChannel | 
my $direction = new WWW::OpenAPIClient.CommunicationDirection(); # CommunicationDirection | 
my $from = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only include communications after this ISO date (inclusive).
my $to = DateTime->from_epoch(epoch => str2time('null')); # DATE | Only include communications before this ISO date (inclusive).

eval {
    my $result = $api_instance->list_communications(page => $page, page_size => $page_size, contact_id => $contact_id, channel => $channel, direction => $direction, from => $from, to => $to);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerCommunicationApi->list_communications: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **contact_id** | **string**| Filter history to a single contact. | [optional] 
 **channel** | [**CommunicationChannel**](.md)|  | [optional] 
 **direction** | [**CommunicationDirection**](.md)|  | [optional] 
 **from** | **DATE**| Only include communications after this ISO date (inclusive). | [optional] 
 **to** | **DATE**| Only include communications before this ISO date (inclusive). | [optional] 

### Return type

[**ARRAY[CustomerCommunication]**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_communication**
> CustomerCommunication update_communication(communication_id => $communication_id, customer_communication_update => $customer_communication_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::CustomerCommunicationApi;
my $api_instance = WWW::OpenAPIClient::CustomerCommunicationApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $communication_id = "communication_id_example"; # string | 
my $customer_communication_update = WWW::OpenAPIClient::Object::CustomerCommunicationUpdate->new(); # CustomerCommunicationUpdate | 

eval {
    my $result = $api_instance->update_communication(communication_id => $communication_id, customer_communication_update => $customer_communication_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling CustomerCommunicationApi->update_communication: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **communication_id** | **string**|  | 
 **customer_communication_update** | [**CustomerCommunicationUpdate**](CustomerCommunicationUpdate.md)|  | 

### Return type

[**CustomerCommunication**](CustomerCommunication.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

