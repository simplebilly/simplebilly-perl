# WWW::OpenAPIClient::PayrollApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PayrollApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**payroll_approve**](PayrollApi.md#payroll_approve) | **POST** /api/v1/payroll/{id}/approve | 
[**payroll_autopay**](PayrollApi.md#payroll_autopay) | **POST** /api/v1/payroll/{id}/autopay | 
[**payroll_calculate**](PayrollApi.md#payroll_calculate) | **POST** /api/v1/payroll/{id}/calculate | 
[**payroll_create**](PayrollApi.md#payroll_create) | **POST** /api/v1/payroll | 
[**payroll_delete**](PayrollApi.md#payroll_delete) | **DELETE** /api/v1/payroll/{id} | 
[**payroll_elster_export**](PayrollApi.md#payroll_elster_export) | **POST** /api/v1/payroll/{id}/elster-export | 
[**payroll_email**](PayrollApi.md#payroll_email) | **POST** /api/v1/payroll/{id}/email | 
[**payroll_entry_pdf**](PayrollApi.md#payroll_entry_pdf) | **GET** /api/v1/payroll/{id}/entries/{entry_id}/pdf | 
[**payroll_get**](PayrollApi.md#payroll_get) | **GET** /api/v1/payroll/{id} | 
[**payroll_list**](PayrollApi.md#payroll_list) | **GET** /api/v1/payroll | 
[**payroll_pay**](PayrollApi.md#payroll_pay) | **POST** /api/v1/payroll/{id}/pay | 
[**payroll_pdf**](PayrollApi.md#payroll_pdf) | **GET** /api/v1/payroll/{id}/pdf | 
[**payroll_summary**](PayrollApi.md#payroll_summary) | **GET** /api/v1/payroll/summary/{year} | 
[**payroll_sv_meldungen**](PayrollApi.md#payroll_sv_meldungen) | **POST** /api/v1/payroll/{id}/sv-meldungen | 


# **payroll_approve**
> PayrollRunApi payroll_approve(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->payroll_approve(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_approve: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_autopay**
> object payroll_autopay(id => $id, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->payroll_autopay(id => $id, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_autopay: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **body** | **object**|  | [optional] 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_calculate**
> PayrollRunApi payroll_calculate(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->payroll_calculate(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_calculate: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_create**
> PayrollRunApi payroll_create(payroll_create_payload => $payroll_create_payload)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $payroll_create_payload = WWW::OpenAPIClient::Object::PayrollCreatePayload->new(); # PayrollCreatePayload | 

eval {
    my $result = $api_instance->payroll_create(payroll_create_payload => $payroll_create_payload);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_create: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payroll_create_payload** | [**PayrollCreatePayload**](PayrollCreatePayload.md)|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_delete**
> payroll_delete(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->payroll_delete(id => $id);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_delete: $@\n";
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_elster_export**
> payroll_elster_export(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->payroll_elster_export(id => $id);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_elster_export: $@\n";
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_email**
> object payroll_email(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->payroll_email(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_email: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_entry_pdf**
> payroll_entry_pdf(id => $id, entry_id => $entry_id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $entry_id = "entry_id_example"; # string | 

eval {
    $api_instance->payroll_entry_pdf(id => $id, entry_id => $entry_id);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_entry_pdf: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **entry_id** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_get**
> PayrollRunApi payroll_get(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->payroll_get(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_get: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_list**
> ARRAY[PayrollRunApi] payroll_list(year => $year, status => $status)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $status = "status_example"; # string | 

eval {
    my $result = $api_instance->payroll_list(year => $year, status => $status);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_list: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **status** | **string**|  | [optional] 

### Return type

[**ARRAY[PayrollRunApi]**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_pay**
> PayrollRunApi payroll_pay(id => $id, payroll_pay_payload => $payroll_pay_payload)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $payroll_pay_payload = WWW::OpenAPIClient::Object::PayrollPayPayload->new(); # PayrollPayPayload | 

eval {
    my $result = $api_instance->payroll_pay(id => $id, payroll_pay_payload => $payroll_pay_payload);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_pay: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **payroll_pay_payload** | [**PayrollPayPayload**](PayrollPayPayload.md)|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_pdf**
> payroll_pdf(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    $api_instance->payroll_pdf(id => $id);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_pdf: $@\n";
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
 - **Accept**: application/pdf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_summary**
> YearlyPayrollSummary payroll_summary(year => $year)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 

eval {
    my $result = $api_instance->payroll_summary(year => $year);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_summary: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | 

### Return type

[**YearlyPayrollSummary**](YearlyPayrollSummary.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **payroll_sv_meldungen**
> object payroll_sv_meldungen(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PayrollApi;
my $api_instance = WWW::OpenAPIClient::PayrollApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->payroll_sv_meldungen(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PayrollApi->payroll_sv_meldungen: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

