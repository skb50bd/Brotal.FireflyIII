# Brotal.FireflyIII.Model.AvailableBudgetProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **DateTime** |  | [optional] [readonly] 
**UpdatedAt** | **DateTime** |  | [optional] [readonly] 
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
**Amount** | **string** | The amount of this available budget in the currency of this available budget. | [optional] 
**PcAmount** | **string** | The amount of this available budget in the primary currency (pc) of this administration. | [optional] 
**Start** | **DateTime** | Start date of the available budget. | [optional] 
**End** | **DateTime** | End date of the available budget. | [optional] 
**SpentInBudgets** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) |  | [optional] [readonly] 
**PcSpentInBudgets** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | The amount spent in budgets in the primary currency (pc) of this administration.  | [optional] [readonly] 
**SpentOutsideBudgets** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) |  | [optional] [readonly] 
**PcSpentOutsideBudgets** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | The amount spent outside of budgets in the primary currency (pc) of this administration.  | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

