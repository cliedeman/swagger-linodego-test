# InvoiceItem

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **int32** | The price, in US dollars, of unit price multiplied by quantity. | [optional] [default to null]
**From** | [**time.Time**](time.Time.md) | The date the Invoice Item started, based on month. | [optional] [default to null]
**Label** | **string** | The Invoice Item&#x27;s display label. | [optional] [default to null]
**Quantity** | **int32** | The quantity of this Item for the specified Invoice. | [optional] [default to null]
**To** | [**time.Time**](time.Time.md) | The date the Invoice Item ended, based on month. | [optional] [default to null]
**Type_** | **string** | The type of service, ether &#x60;prepay&#x60; or &#x60;misc&#x60;. | [optional] [default to null]
**Unitprice** | **int32** | The monthly service fee in US Dollars for this Item. | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

