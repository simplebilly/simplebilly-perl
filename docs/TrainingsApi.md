# WWW::OpenAPIClient::TrainingsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::TrainingsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_my_trainings**](TrainingsApi.md#get_my_trainings) | **GET** /api/v1/trainings/me | 
[**get_training_content**](TrainingsApi.md#get_training_content) | **GET** /api/v1/trainings/content/{code} | 
[**get_training_overview**](TrainingsApi.md#get_training_overview) | **GET** /api/v1/trainings/overview | 
[**submit_training_result**](TrainingsApi.md#submit_training_result) | **POST** /api/v1/trainings/submit-result | 


# **get_my_trainings**
> ARRAY[MyTrainingItem] get_my_trainings()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingsApi;
my $api_instance = WWW::OpenAPIClient::TrainingsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_my_trainings();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingsApi->get_my_trainings: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[MyTrainingItem]**](MyTrainingItem.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_training_content**
> TrainingContent get_training_content(code => $code)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingsApi;
my $api_instance = WWW::OpenAPIClient::TrainingsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $code = "code_example"; # string | Training code, e.g. data_privacy

eval {
    my $result = $api_instance->get_training_content(code => $code);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingsApi->get_training_content: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **code** | **string**| Training code, e.g. data_privacy | 

### Return type

[**TrainingContent**](TrainingContent.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_training_overview**
> ARRAY[HrTrainingOverview] get_training_overview()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingsApi;
my $api_instance = WWW::OpenAPIClient::TrainingsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_training_overview();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingsApi->get_training_overview: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[HrTrainingOverview]**](HrTrainingOverview.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **submit_training_result**
> SubmitResultResponse submit_training_result(submit_result_dto => $submit_result_dto)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TrainingsApi;
my $api_instance = WWW::OpenAPIClient::TrainingsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $submit_result_dto = WWW::OpenAPIClient::Object::SubmitResultDto->new(); # SubmitResultDto | 

eval {
    my $result = $api_instance->submit_training_result(submit_result_dto => $submit_result_dto);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TrainingsApi->submit_training_result: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **submit_result_dto** | [**SubmitResultDto**](SubmitResultDto.md)|  | 

### Return type

[**SubmitResultResponse**](SubmitResultResponse.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

