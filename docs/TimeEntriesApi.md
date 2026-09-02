# WWW::OpenAPIClient::TimeEntriesApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::TimeEntriesApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**clock_in_time_entry**](TimeEntriesApi.md#clock_in_time_entry) | **POST** /api/v1/time-entries | Clock in for the authenticated user (resolved via their employee profile).
[**clock_out_time_entry**](TimeEntriesApi.md#clock_out_time_entry) | **PATCH** /api/v1/time-entries/{id} | Clock out an entry: the entry&#39;s owner, or anyone with &#x60;time_entries:write&#x60;.
[**get_labor_costs**](TimeEntriesApi.md#get_labor_costs) | **GET** /api/v1/labor-costs | Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee&#39;s hourly cost rate.
[**list_time_entries**](TimeEntriesApi.md#list_time_entries) | **GET** /api/v1/time-entries | List time entries with optional date-range / active / employee filters.


# **clock_in_time_entry**
> TimeEntryDto clock_in_time_entry(time_entry_clock_in => $time_entry_clock_in)

Clock in for the authenticated user (resolved via their employee profile).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TimeEntriesApi;
my $api_instance = WWW::OpenAPIClient::TimeEntriesApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $time_entry_clock_in = WWW::OpenAPIClient::Object::TimeEntryClockIn->new(); # TimeEntryClockIn | 

eval {
    my $result = $api_instance->clock_in_time_entry(time_entry_clock_in => $time_entry_clock_in);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TimeEntriesApi->clock_in_time_entry: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **time_entry_clock_in** | [**TimeEntryClockIn**](TimeEntryClockIn.md)|  | 

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **clock_out_time_entry**
> TimeEntryDto clock_out_time_entry(id => $id, time_entry_clock_out => $time_entry_clock_out)

Clock out an entry: the entry's owner, or anyone with `time_entries:write`.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TimeEntriesApi;
my $api_instance = WWW::OpenAPIClient::TimeEntriesApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 
my $time_entry_clock_out = WWW::OpenAPIClient::Object::TimeEntryClockOut->new(); # TimeEntryClockOut | 

eval {
    my $result = $api_instance->clock_out_time_entry(id => $id, time_entry_clock_out => $time_entry_clock_out);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TimeEntriesApi->clock_out_time_entry: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 
 **time_entry_clock_out** | [**TimeEntryClockOut**](TimeEntryClockOut.md)|  | 

### Return type

[**TimeEntryDto**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_labor_costs**
> ARRAY[LaborCostRow] get_labor_costs(from => $from, to => $to, group_by => $group_by)

Labor-cost report: worked hours aggregated per employee / order / day, valued at the employee's hourly cost rate.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TimeEntriesApi;
my $api_instance = WWW::OpenAPIClient::TimeEntriesApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $from = DateTime->from_epoch(epoch => str2time('null')); # DATE | 
my $to = DateTime->from_epoch(epoch => str2time('null')); # DATE | 
my $group_by = "group_by_example"; # string | One of \"employee\", \"order\" or \"day\".

eval {
    my $result = $api_instance->get_labor_costs(from => $from, to => $to, group_by => $group_by);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TimeEntriesApi->get_labor_costs: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **from** | **DATE**|  | 
 **to** | **DATE**|  | 
 **group_by** | **string**| One of \&quot;employee\&quot;, \&quot;order\&quot; or \&quot;day\&quot;. | 

### Return type

[**ARRAY[LaborCostRow]**](LaborCostRow.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_time_entries**
> ARRAY[TimeEntryDto] list_time_entries(from => $from, to => $to, active => $active, employee_id => $employee_id)

List time entries with optional date-range / active / employee filters.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::TimeEntriesApi;
my $api_instance = WWW::OpenAPIClient::TimeEntriesApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $from = DateTime->from_epoch(epoch => str2time('null')); # DATE | 
my $to = DateTime->from_epoch(epoch => str2time('null')); # DATE | 
my $active = null; # boolean | Only currently running shifts (clock_in set, clock_out null).
my $employee_id = "employee_id_example"; # string | 

eval {
    my $result = $api_instance->list_time_entries(from => $from, to => $to, active => $active, employee_id => $employee_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling TimeEntriesApi->list_time_entries: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **from** | **DATE**|  | [optional] 
 **to** | **DATE**|  | [optional] 
 **active** | **boolean**| Only currently running shifts (clock_in set, clock_out null). | [optional] 
 **employee_id** | **string**|  | [optional] 

### Return type

[**ARRAY[TimeEntryDto]**](TimeEntryDto.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

