# Account

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address1** | **string** | First line of this Account&#x27;s billing address. | [optional] [default to null]
**Address2** | **string** | Second line of this Account&#x27;s billing address. | [optional] [default to null]
**Balance** | [***BigDecimal**](BigDecimal.md) | This Account&#x27;s balance, in US dollars. | [optional] [default to null]
**City** | **string** | The city for this Account&#x27;s billing address. | [optional] [default to null]
**CreditCard** | [***AccountCreditCard**](Account_credit_card.md) |  | [optional] [default to null]
**Company** | **string** | The company name associated with this Account. | [optional] [default to null]
**Country** | **string** | The two-letter country code of this Account&#x27;s billing address.  | [optional] [default to null]
**Email** | **string** | The email address of the person associated with this Account. | [optional] [default to null]
**FirstName** | **string** | The first name of the person associated with this Account. | [optional] [default to null]
**LastName** | **string** | The last name of the person associated with this Account. | [optional] [default to null]
**Phone** | **string** | The phone number associated with this Account. | [optional] [default to null]
**State** | **string** | If billing address is in the United States, this is the State portion of the Account&#x27;s billing address. If the address is outside the US, this is the Province associated with the Account&#x27;s billing address.  | [optional] [default to null]
**TaxId** | **string** | The tax identification number associated with this Account, for tax calculations in some countries. If you do not live in a country that collects tax, this should be &#x60;null&#x60;.  | [optional] [default to null]
**Zip** | **string** | The zip code of this Account&#x27;s billing address. | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

