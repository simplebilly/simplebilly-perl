# WWW::OpenAPIClient::BookkeepingApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::BookkeepingApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**allocate_payment_api**](BookkeepingApi.md#allocate_payment_api) | **POST** /api/v1/payments/allocate | Allocate a payment to an invoice
[**bwa_report_api**](BookkeepingApi.md#bwa_report_api) | **GET** /api/v1/bookkeeping/bwa | Get BWA (Betriebswirtschaftliche Auswertung) report
[**elster_status_api**](BookkeepingApi.md#elster_status_api) | **GET** /api/v1/bookkeeping/elster/status | 
[**elster_validate_api**](BookkeepingApi.md#elster_validate_api) | **POST** /api/v1/bookkeeping/ustva/elster-validate | 
[**elster_xml_api**](BookkeepingApi.md#elster_xml_api) | **GET** /api/v1/bookkeeping/ustva/elster-xml | 
[**get_cashflow**](BookkeepingApi.md#get_cashflow) | **GET** /api/v1/bookkeeping/cashflow | GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
[**get_liquidity**](BookkeepingApi.md#get_liquidity) | **GET** /api/v1/bookkeeping/liquidity | GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
[**get_open_invoices_api**](BookkeepingApi.md#get_open_invoices_api) | **GET** /api/v1/payments/open-invoices/{customer_id} | Get open invoices for a customer
[**get_verfahrensdokumentation**](BookkeepingApi.md#get_verfahrensdokumentation) | **GET** /api/v1/bookkeeping/verfahrensdokumentation | GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
[**run_dunning_api**](BookkeepingApi.md#run_dunning_api) | **POST** /api/v1/bookkeeping/dunning | 


# **allocate_payment_api**
> allocate_payment_api(allocate_payment_request => $allocate_payment_request)

Allocate a payment to an invoice

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $allocate_payment_request = WWW::OpenAPIClient::Object::AllocatePaymentRequest->new(); # AllocatePaymentRequest | 

eval {
    $api_instance->allocate_payment_api(allocate_payment_request => $allocate_payment_request);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->allocate_payment_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **allocate_payment_request** | [**AllocatePaymentRequest**](AllocatePaymentRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bwa_report_api**
> BWAReport bwa_report_api(year => $year, month => $month)

Get BWA (Betriebswirtschaftliche Auswertung) report

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 

eval {
    my $result = $api_instance->bwa_report_api(year => $year, month => $month);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->bwa_report_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **month** | **int**|  | [optional] 

### Return type

[**BWAReport**](BWAReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **elster_status_api**
> ElsterStatus elster_status_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->elster_status_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->elster_status_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ElsterStatus**](ElsterStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **elster_validate_api**
> elster_validate_api(zeitraum => $zeitraum)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $zeitraum = "zeitraum_example"; # string | 

eval {
    $api_instance->elster_validate_api(zeitraum => $zeitraum);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->elster_validate_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **zeitraum** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **elster_xml_api**
> elster_xml_api(zeitraum => $zeitraum)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $zeitraum = "zeitraum_example"; # string | 

eval {
    $api_instance->elster_xml_api(zeitraum => $zeitraum);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->elster_xml_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **zeitraum** | **string**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_cashflow**
> CashflowReport get_cashflow(year => $year, month => $month)

GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $year = 56; # int | 
my $month = 56; # int | 

eval {
    my $result = $api_instance->get_cashflow(year => $year, month => $month);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->get_cashflow: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **year** | **int**|  | [optional] 
 **month** | **int**|  | [optional] 

### Return type

[**CashflowReport**](CashflowReport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_liquidity**
> LiquidityPosition get_liquidity()

GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_liquidity();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->get_liquidity: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**LiquidityPosition**](LiquidityPosition.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_open_invoices_api**
> ARRAY[Invoice] get_open_invoices_api(customer_id => $customer_id)

Get open invoices for a customer

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $customer_id = "customer_id_example"; # string | 

eval {
    my $result = $api_instance->get_open_invoices_api(customer_id => $customer_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->get_open_invoices_api: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **customer_id** | **string**|  | 

### Return type

[**ARRAY[Invoice]**](Invoice.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_verfahrensdokumentation**
> Verfahrensdokumentation get_verfahrensdokumentation()

GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_verfahrensdokumentation();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->get_verfahrensdokumentation: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Verfahrensdokumentation**](Verfahrensdokumentation.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **run_dunning_api**
> DunningResult run_dunning_api()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::BookkeepingApi;
my $api_instance = WWW::OpenAPIClient::BookkeepingApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->run_dunning_api();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling BookkeepingApi->run_dunning_api: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**DunningResult**](DunningResult.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

