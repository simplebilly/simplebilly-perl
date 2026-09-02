# WWW::OpenAPIClient::GdprApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::GdprApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_dpa**](GdprApi.md#accept_dpa) | **PUT** /api/v1/gdpr/dpa | Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).
[**account_erasure**](GdprApi.md#account_erasure) | **POST** /api/v1/gdpr/account-erasure | Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).
[**erasure_contact**](GdprApi.md#erasure_contact) | **POST** /api/v1/gdpr/erasure/{contact_id} | Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on &#x60;contacts&#x60; already records who/when.
[**export_contact_data**](GdprApi.md#export_contact_data) | **GET** /api/v1/gdpr/export/{contact_id} | Art. 15 data-subject access export for a contact.
[**export_gdpr**](GdprApi.md#export_gdpr) | **GET** /api/v1/gdpr/export | Export the current user&#39;s personal data (GDPR Art. 15/20).
[**get_dpa**](GdprApi.md#get_dpa) | **GET** /api/v1/gdpr/dpa | Current DPA acceptance status (from tenant_settings).


# **accept_dpa**
> DpaStatus accept_dpa(dpa_accept_request => $dpa_accept_request)

Record DPA acceptance: sets dpa_accepted_at/by/version on the tenant settings row (created with company-type defaults if missing).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GdprApi;
my $api_instance = WWW::OpenAPIClient::GdprApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $dpa_accept_request = WWW::OpenAPIClient::Object::DpaAcceptRequest->new(); # DpaAcceptRequest | 

eval {
    my $result = $api_instance->accept_dpa(dpa_accept_request => $dpa_accept_request);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GdprApi->accept_dpa: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dpa_accept_request** | [**DpaAcceptRequest**](DpaAcceptRequest.md)|  | 

### Return type

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **account_erasure**
> object account_erasure()

Erase ALL personal data of the tenant (TOS §11: deletion 90 days after termination).

Anonymizes every contact, anonymizes personal fields on bookkeeping records (orders/invoices/payments keep amounts and dates for GoBD), removes the tenant linkage of the (global, saasy-framework) users and marks the erasure on `tenant_settings.gdpr_erased_at`. No row is physically deleted. The audit triggers on the touched tables record who/when.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GdprApi;
my $api_instance = WWW::OpenAPIClient::GdprApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->account_erasure();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GdprApi->account_erasure: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **erasure_contact**
> object erasure_contact(contact_id => $contact_id)

Anonymize + soft-delete a contact: personal attributes are cleared, the record itself is kept for GoBD retention (Art. 17(3)(e) DSGVO). The audit trigger on `contacts` already records who/when.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GdprApi;
my $api_instance = WWW::OpenAPIClient::GdprApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $contact_id = "contact_id_example"; # string | 

eval {
    my $result = $api_instance->erasure_contact(contact_id => $contact_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GdprApi->erasure_contact: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_id** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_contact_data**
> object export_contact_data(contact_id => $contact_id)

Art. 15 data-subject access export for a contact.

Returns the contact itself plus the tenant-scoped rows linked to it.  ## Relations The `customers`/`orders`/`invoices`/`payments` tables have no FK to `contacts`; they are linked through the `customer_id` column, which per the app's conventions holds one of: - the admin customer's `customer_id` (a UUID, often the same value as   the contact's `contact_id`/`customer_number`), - the buyer's email for shop orders, or - the marketplace's external customer id for plugin orders.  The export therefore matches the contact's identifiers (`contact_id`, `customer_number`, `external_id`, `email`) plus any resolved customer ids against `customer_id`. `delivery_notes` and `customer_communications` reference contacts directly via `contact_id`. Soft-deleted rows are included (their data is still processed and retained for GoBD). Relations that genuinely do not exist for a contact stay empty but the key is always present.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GdprApi;
my $api_instance = WWW::OpenAPIClient::GdprApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $contact_id = "contact_id_example"; # string | 

eval {
    my $result = $api_instance->export_contact_data(contact_id => $contact_id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GdprApi->export_contact_data: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contact_id** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_gdpr**
> ApiResponseGdprExport export_gdpr()

Export the current user's personal data (GDPR Art. 15/20).

No admin permission required: a user always exports their own data.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GdprApi;
my $api_instance = WWW::OpenAPIClient::GdprApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->export_gdpr();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GdprApi->export_gdpr: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseGdprExport**](ApiResponseGdprExport.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_dpa**
> DpaStatus get_dpa()

Current DPA acceptance status (from tenant_settings).

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::GdprApi;
my $api_instance = WWW::OpenAPIClient::GdprApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_dpa();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling GdprApi->get_dpa: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**DpaStatus**](DpaStatus.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

