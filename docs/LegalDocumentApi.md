# WWW::OpenAPIClient::LegalDocumentApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::LegalDocumentApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_legal_documents**](LegalDocumentApi.md#get_legal_documents) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.
[**reset_legal_documents**](LegalDocumentApi.md#reset_legal_documents) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.
[**upsert_legal_documents**](LegalDocumentApi.md#upsert_legal_documents) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list.


# **get_legal_documents**
> ARRAY[LegalDocument] get_legal_documents()

List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::LegalDocumentApi;
my $api_instance = WWW::OpenAPIClient::LegalDocumentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->get_legal_documents();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling LegalDocumentApi->get_legal_documents: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[LegalDocument]**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_legal_documents**
> ARRAY[LegalDocument] reset_legal_documents(legal_document_reset => $legal_document_reset)

Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::LegalDocumentApi;
my $api_instance = WWW::OpenAPIClient::LegalDocumentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $legal_document_reset = WWW::OpenAPIClient::Object::LegalDocumentReset->new(); # LegalDocumentReset | 

eval {
    my $result = $api_instance->reset_legal_documents(legal_document_reset => $legal_document_reset);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling LegalDocumentApi->reset_legal_documents: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **legal_document_reset** | [**LegalDocumentReset**](LegalDocumentReset.md)|  | 

### Return type

[**ARRAY[LegalDocument]**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsert_legal_documents**
> ARRAY[LegalDocument] upsert_legal_documents(legal_document_upsert => $legal_document_upsert)

Upsert legal documents per (doc_type, lang). Returns the full tenant list.

### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::LegalDocumentApi;
my $api_instance = WWW::OpenAPIClient::LegalDocumentApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $legal_document_upsert = [WWW::OpenAPIClient::Object::ARRAY[LegalDocumentUpsert]->new()]; # ARRAY[LegalDocumentUpsert] | 

eval {
    my $result = $api_instance->upsert_legal_documents(legal_document_upsert => $legal_document_upsert);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling LegalDocumentApi->upsert_legal_documents: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **legal_document_upsert** | [**ARRAY[LegalDocumentUpsert]**](LegalDocumentUpsert.md)|  | 

### Return type

[**ARRAY[LegalDocument]**](LegalDocument.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

