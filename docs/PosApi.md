# WWW::OpenAPIClient::PosApi

## Load the API package
```perl
use WWW::OpenAPIClient::Object::PosApi;
```

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pos_billing**](PosApi.md#pos_billing) | **GET** /api/pos/billing | 
[**pos_create_order**](PosApi.md#pos_create_order) | **POST** /api/pos/orders | 
[**pos_create_register**](PosApi.md#pos_create_register) | **POST** /api/pos/registers | 
[**pos_create_table**](PosApi.md#pos_create_table) | **POST** /api/pos/tables | 
[**pos_disable_register**](PosApi.md#pos_disable_register) | **POST** /api/pos/registers/{id}/disable | 
[**pos_free_table**](PosApi.md#pos_free_table) | **POST** /api/pos/tables/{id}/free | 
[**pos_kasse_closing**](PosApi.md#pos_kasse_closing) | **POST** /api/pos/kasse/closing | 
[**pos_kasse_entries**](PosApi.md#pos_kasse_entries) | **GET** /api/pos/kasse/entries | 
[**pos_kasse_export**](PosApi.md#pos_kasse_export) | **GET** /api/pos/kasse/export | 
[**pos_kasse_pay_in_out**](PosApi.md#pos_kasse_pay_in_out) | **POST** /api/pos/kasse/pay-in-out | 
[**pos_list_orders**](PosApi.md#pos_list_orders) | **GET** /api/pos/orders | 
[**pos_list_products**](PosApi.md#pos_list_products) | **GET** /api/pos/products | 
[**pos_list_registers**](PosApi.md#pos_list_registers) | **GET** /api/pos/registers | 
[**pos_list_tables**](PosApi.md#pos_list_tables) | **GET** /api/pos/tables | 
[**pos_order_print**](PosApi.md#pos_order_print) | **GET** /api/pos/orders/{order_number}/print | 
[**pos_order_receipt**](PosApi.md#pos_order_receipt) | **GET** /api/pos/orders/{order_number}/receipt | 
[**pos_pay_order**](PosApi.md#pos_pay_order) | **POST** /api/pos/orders/{order_number}/pay | 
[**pos_sumup_checkout**](PosApi.md#pos_sumup_checkout) | **POST** /api/pos/sumup/checkout | 


# **pos_billing**
> object pos_billing()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->pos_billing();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_billing: $@\n";
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

# **pos_create_order**
> object pos_create_order(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->pos_create_order(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_create_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_create_register**
> PosRegister pos_create_register(pos_register_create => $pos_register_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $pos_register_create = WWW::OpenAPIClient::Object::PosRegisterCreate->new(); # PosRegisterCreate | 

eval {
    my $result = $api_instance->pos_create_register(pos_register_create => $pos_register_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_create_register: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pos_register_create** | [**PosRegisterCreate**](PosRegisterCreate.md)|  | 

### Return type

[**PosRegister**](PosRegister.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_create_table**
> PosTable pos_create_table(pos_table_create => $pos_table_create)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $pos_table_create = WWW::OpenAPIClient::Object::PosTableCreate->new(); # PosTableCreate | 

eval {
    my $result = $api_instance->pos_create_table(pos_table_create => $pos_table_create);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_create_table: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pos_table_create** | [**PosTableCreate**](PosTableCreate.md)|  | 

### Return type

[**PosTable**](PosTable.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_disable_register**
> PosRegister pos_disable_register(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->pos_disable_register(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_disable_register: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**PosRegister**](PosRegister.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_free_table**
> PosTable pos_free_table(id => $id)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $id = "id_example"; # string | 

eval {
    my $result = $api_instance->pos_free_table(id => $id);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_free_table: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **string**|  | 

### Return type

[**PosTable**](PosTable.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_kasse_closing**
> object pos_kasse_closing(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->pos_kasse_closing(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_kasse_closing: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_kasse_entries**
> object pos_kasse_entries()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->pos_kasse_entries();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_kasse_entries: $@\n";
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

# **pos_kasse_export**
> object pos_kasse_export()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->pos_kasse_export();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_kasse_export: $@\n";
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

# **pos_kasse_pay_in_out**
> object pos_kasse_pay_in_out(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->pos_kasse_pay_in_out(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_kasse_pay_in_out: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_list_orders**
> object pos_list_orders(status => $status)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $status = "status_example"; # string | Filter by order status

eval {
    my $result = $api_instance->pos_list_orders(status => $status);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_list_orders: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **string**| Filter by order status | [optional] 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_list_products**
> object pos_list_products(q => $q)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $q = "q_example"; # string | Product search

eval {
    my $result = $api_instance->pos_list_products(q => $q);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_list_products: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **string**| Product search | [optional] 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_list_registers**
> ARRAY[PosRegister] pos_list_registers()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->pos_list_registers();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_list_registers: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[PosRegister]**](PosRegister.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_list_tables**
> ARRAY[PosTable] pos_list_tables()



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);


eval {
    my $result = $api_instance->pos_list_tables();
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_list_tables: $@\n";
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ARRAY[PosTable]**](PosTable.md)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_order_print**
> object pos_order_print(order_number => $order_number)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->pos_order_print(order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_order_print: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_order_receipt**
> object pos_order_receipt(order_number => $order_number)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 

eval {
    my $result = $api_instance->pos_order_receipt(order_number => $order_number);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_order_receipt: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_pay_order**
> object pos_pay_order(order_number => $order_number, body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $order_number = "order_number_example"; # string | 
my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->pos_pay_order(order_number => $order_number, body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_pay_order: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **order_number** | **string**|  | 
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pos_sumup_checkout**
> object pos_sumup_checkout(body => $body)



### Example
```perl
use Data::Dumper;
use WWW::OpenAPIClient::PosApi;
my $api_instance = WWW::OpenAPIClient::PosApi->new(

    # Configure bearer access token for authorization: bearer_token
    access_token => 'YOUR_BEARER_TOKEN',
    
);

my $body = WWW::OpenAPIClient::Object::object->new(); # object | 

eval {
    my $result = $api_instance->pos_sumup_checkout(body => $body);
    print Dumper($result);
};
if ($@) {
    warn "Exception when calling PosApi->pos_sumup_checkout: $@\n";
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **object**|  | 

### Return type

**object**

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

