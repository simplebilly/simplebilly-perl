# WWW::OpenAPIClient::Object::DeclarationCreate

## Load the model package
```perl
use WWW::OpenAPIClient::Object::DeclarationCreate;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**declaration_type** | [**DeclarationType**](DeclarationType.md) | Art der Erklärung: \&quot;dcgk\&quot; (Entsprechenserklärung § 161 AktG) oder \&quot;unternehmensfuehrung\&quot; (Erklärung zur Unternehmensführung § 289f HGB). | [optional] 
**is_current** | **boolean** | Kennzeichnet die aktuell gültige Fassung (max. eine je Mandant). | [optional] 
**text** | **string** | Inhalt der Erklärung als Markdown. | [optional] 
**valid_from** | **DATE** | Datum, ab dem die Erklärung gilt. | [optional] 
**version** | **string** | Versionsbezeichnung der Erklärung (z.B. \&quot;2025-01\&quot;). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


