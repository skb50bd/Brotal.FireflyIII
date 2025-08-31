# Brotal.FireflyIII.Model.RecurrenceTransaction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **string** |  | 
**Amount** | **string** | Amount of the transaction. | 
**Id** | **string** |  | [optional] 
**ObjectHasCurrencySetting** | **bool** | Indicates whether the object has a currency setting. If false, the object uses the administration&#39;s primary currency. | [optional] [readonly] 
**CurrencyId** | **string** | The currency ID of the currency associated with this object. | [optional] 
**CurrencyName** | **string** | The currency name of the currency associated with this object. | [optional] 
**CurrencyCode** | **string** | The currency code of the currency associated with this object. | [optional] 
**CurrencySymbol** | **string** |  | [optional] [readonly] 
**CurrencyDecimalPlaces** | **int** |  | [optional] [readonly] 
**PrimaryCurrencyId** | **string** | The currency ID of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencyName** | **string** | The currency name of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencyCode** | **string** | The currency code of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencySymbol** | **string** | The currency symbol of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencyDecimalPlaces** | **int** | The currency decimal places of the administration&#39;s primary currency. | [optional] [readonly] 
**PcAmount** | **string** | Amount of the transaction in primary currency. | [optional] 
**ForeignAmount** | **string** | Foreign amount of the transaction. | [optional] 
**PcForeignAmount** | **string** | Foreign amount of the transaction. | [optional] 
**ForeignCurrencyId** | **string** |  | [optional] 
**ForeignCurrencyName** | **string** |  | [optional] 
**ForeignCurrencyCode** | **string** |  | [optional] 
**ForeignCurrencySymbol** | **string** |  | [optional] [readonly] 
**ForeignCurrencyDecimalPlaces** | **int** | Number of decimals in the currency | [optional] [readonly] 
**BudgetId** | **string** | The budget ID for this transaction. | [optional] 
**BudgetName** | **string** | The name of the budget to be used. If the budget name is unknown, the ID will be used or the value will be ignored. | [optional] [readonly] 
**CategoryId** | **string** | Category ID for this transaction. | [optional] 
**CategoryName** | **string** | Category name for this transaction. | [optional] 
**SourceId** | **string** | ID of the source account. Submit either this or source_name. | [optional] 
**SourceName** | **string** | Name of the source account. Submit either this or source_id. | [optional] 
**SourceIban** | **string** |  | [optional] [readonly] 
**SourceType** | **AccountTypeProperty** |  | [optional] 
**DestinationId** | **string** | ID of the destination account. Submit either this or destination_name. | [optional] 
**DestinationName** | **string** | Name of the destination account. Submit either this or destination_id. | [optional] 
**DestinationIban** | **string** |  | [optional] [readonly] 
**DestinationType** | **AccountTypeProperty** |  | [optional] 
**Tags** | **List&lt;string&gt;** | Array of tags. | [optional] 
**PiggyBankId** | **string** |  | [optional] 
**PiggyBankName** | **string** |  | [optional] 
**SubscriptionId** | **string** |  | [optional] 
**SubscriptionName** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

