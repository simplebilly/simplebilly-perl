# WWW::OpenAPIClient::Object::ReturnLogisticsSummary

## Load the model package
```perl
use WWW::OpenAPIClient::Object::ReturnLogisticsSummary;
```

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**by_status** | **object** | Number of return orders per status. | 
**by_warehouse** | [**ARRAY[ReturnWarehouseSummary]**](ReturnWarehouseSummary.md) | Per-warehouse aggregation. | 
**items_restocked** | **int** | Sum of &#x60;restock: true&#x60; line-item quantities. | 
**items_scrapped** | **int** | Sum of &#x60;restock: false&#x60; line-item quantities (scrapped/disposed). | 
**total_items** | **int** | Sum of all line-item quantities across returns. | 
**total_returns** | **int** | Total number of return orders (excluding soft-deleted). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


