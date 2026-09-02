# WWW::OpenAPIClient::BudgetsApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::BudgetsApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**budgets_api**](BudgetsApi.md#budgets_api) | **GET** /api/v1/bookkeeping/budgets | 
[**upsert_budget_goal_api**](BudgetsApi.md#upsert_budget_goal_api) | **PUT** /api/v1/bookkeeping/budgets/goals/{category} | 


# **budgets_api**
> BudgetErgebnis budgets_api(year => $year, month => $month)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BudgetsApi;
my $api_instance = WWW::OpenAPIClient::BudgetsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 

eval {
    my $result = $api_instance->budgets_api(year => $year, month => $month);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BudgetsApi->budgets_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 
 **month** | **int**|  | 

### Return type

[**BudgetErgebnis**](BudgetErgebnis.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsert_budget_goal_api**
> Budget upsert_budget_goal_api(category => $category, budget_goal_request => $budget_goal_request)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BudgetsApi;
my $api_instance = WWW::OpenAPIClient::BudgetsApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $category = "category_example"; # string | 
my $budget_goal_request = WWW::OpenAPIClient::Object::BudgetGoalRequest->new(); # BudgetGoalRequest | 

eval {
    my $result = $api_instance->upsert_budget_goal_api(category => $category, budget_goal_request => $budget_goal_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BudgetsApi->upsert_budget_goal_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category** | **string**|  | 
 **budget_goal_request** | [**BudgetGoalRequest**](BudgetGoalRequest.md)|  | 

### Return type

[**Budget**](Budget.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

