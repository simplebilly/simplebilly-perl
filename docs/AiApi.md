# WWW::OpenAPIClient::AiApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::AiApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ai_suggest_api**](AiApi.md#ai_suggest_api) | **POST** /api/v1/support/ai/suggest | 
[**create_worker_api**](AiApi.md#create_worker_api) | **POST** /api/v1/support/ai/workers | 
[**list_workers_api**](AiApi.md#list_workers_api) | **GET** /api/v1/support/ai/workers | 
[**run_worker_api**](AiApi.md#run_worker_api) | **POST** /api/v1/support/ai/workers/{worker_id}/run | 


# **ai_suggest_api**
> AiSuggestion ai_suggest_api(ai_suggestion_request => $ai_suggestion_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AiApi;
my $api_instance = WWW::OpenAPIClient::AiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ai_suggestion_request = WWW::OpenAPIClient::Object::AiSuggestionRequest->new(); # AiSuggestionRequest | 

eval {
    my $result = $api_instance->ai_suggest_api(ai_suggestion_request => $ai_suggestion_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AiApi->ai_suggest_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ai_suggestion_request** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  | 

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_worker_api**
> AiWorkerConfig create_worker_api(ai_config_dto => $ai_config_dto)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AiApi;
my $api_instance = WWW::OpenAPIClient::AiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $ai_config_dto = WWW::OpenAPIClient::Object::AiConfigDto->new(); # AiConfigDto | 

eval {
    my $result = $api_instance->create_worker_api(ai_config_dto => $ai_config_dto);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AiApi->create_worker_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ai_config_dto** | [**AiConfigDto**](AiConfigDto.md)|  | 

### Return type

[**AiWorkerConfig**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_workers_api**
> ARRAY[AiWorkerConfig] list_workers_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AiApi;
my $api_instance = WWW::OpenAPIClient::AiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->list_workers_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AiApi->list_workers_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[AiWorkerConfig]**](AiWorkerConfig.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **run_worker_api**
> AiSuggestion run_worker_api(worker_id => $worker_id, ai_suggestion_request => $ai_suggestion_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::AiApi;
my $api_instance = WWW::OpenAPIClient::AiApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $worker_id = "worker_id_example"; # string | 
my $ai_suggestion_request = WWW::OpenAPIClient::Object::AiSuggestionRequest->new(); # AiSuggestionRequest | 

eval {
    my $result = $api_instance->run_worker_api(worker_id => $worker_id, ai_suggestion_request => $ai_suggestion_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling AiApi->run_worker_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **worker_id** | **string**|  | 
 **ai_suggestion_request** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  | 

### Return type

[**AiSuggestion**](AiSuggestion.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

