# WWW::OpenAPIClient::EmployeeApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::EmployeeApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_employee**](EmployeeApi.md#create_employee) | **POST** /api/v1/employees | 
[**delete_employee**](EmployeeApi.md#delete_employee) | **DELETE** /api/v1/employees/{id} | 
[**employee_restore**](EmployeeApi.md#employee_restore) | **POST** /api/v1/employees/{id}/restore | 
[**get_employee**](EmployeeApi.md#get_employee) | **GET** /api/v1/employees/{id} | 
[**get_employee_payroll_summary**](EmployeeApi.md#get_employee_payroll_summary) | **GET** /api/v1/employees/{id}/payroll-summary | 
[**get_employees**](EmployeeApi.md#get_employees) | **GET** /api/v1/employees/ | 
[**update_employee**](EmployeeApi.md#update_employee) | **PUT** /api/v1/employees/{id} | 


# **create_employee**
> Employee create_employee(employee_create => $employee_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmployeeApi;
my $api_instance = WWW::OpenAPIClient::EmployeeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $employee_create = WWW::OpenAPIClient::Object::EmployeeCreate->new(); # EmployeeCreate | 

eval {
    my $result = $api_instance->create_employee(employee_create => $employee_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmployeeApi->create_employee: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employee_create** | [**EmployeeCreate**](EmployeeCreate.md)|  | 

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_employee**
> delete_employee(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmployeeApi;
my $api_instance = WWW::OpenAPIClient::EmployeeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->delete_employee(id => $id);
};
if ($@) {
    warn "Exception when calling EmployeeApi->delete_employee: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **employee_restore**
> Employee employee_restore(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmployeeApi;
my $api_instance = WWW::OpenAPIClient::EmployeeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->employee_restore(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmployeeApi->employee_restore: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_employee**
> Employee get_employee(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmployeeApi;
my $api_instance = WWW::OpenAPIClient::EmployeeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->get_employee(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmployeeApi->get_employee: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_employee_payroll_summary**
> PayrollSummary get_employee_payroll_summary(id => $id, year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmployeeApi;
my $api_instance = WWW::OpenAPIClient::EmployeeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $year = 56; # int | Fiscal year for the breakdown; defaults to the current year.

eval {
    my $result = $api_instance->get_employee_payroll_summary(id => $id, year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmployeeApi->get_employee_payroll_summary: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **year** | **int**| Fiscal year for the breakdown; defaults to the current year. | [optional] 

### Return type

[**PayrollSummary**](PayrollSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_employees**
> ARRAY[Employee] get_employees(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmployeeApi;
my $api_instance = WWW::OpenAPIClient::EmployeeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $page = 1; # int | 
my $page_size = 56; # int | 
my $search = "search_example"; # string | 
my $include_deleted = null; # boolean | Soft-delete entities: set true to include rows with `deleted_at` set.

eval {
    my $result = $api_instance->get_employees(page => $page, page_size => $page_size, search => $search, include_deleted => $include_deleted);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmployeeApi->get_employees: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **page_size** | **int**|  | [optional] 
 **search** | **string**|  | [optional] 
 **include_deleted** | **boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**ARRAY[Employee]**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_employee**
> Employee update_employee(id => $id, employee_update => $employee_update)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::EmployeeApi;
my $api_instance = WWW::OpenAPIClient::EmployeeApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $employee_update = WWW::OpenAPIClient::Object::EmployeeUpdate->new(); # EmployeeUpdate | 

eval {
    my $result = $api_instance->update_employee(id => $id, employee_update => $employee_update);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling EmployeeApi->update_employee: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **employee_update** | [**EmployeeUpdate**](EmployeeUpdate.md)|  | 

### Return type

[**Employee**](Employee.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

