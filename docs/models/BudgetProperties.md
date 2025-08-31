# Brotal.FireflyIII.Model.BudgetProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**CreatedAt** | **DateTime** |  | [optional] [readonly] 
**UpdatedAt** | **DateTime** |  | [optional] [readonly] 
**Active** | **bool** |  | [optional] 
**Order** | **int** |  | [optional] [readonly] 
**Notes** | **string** |  | [optional] 
**AutoBudgetType** | **AutoBudgetType** |  | [optional] 
**AutoBudgetPeriod** | **AutoBudgetPeriod** |  | [optional] 
**ObjectGroupId** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] 
**ObjectGroupOrder** | **int** | The order of the group. At least 1, for the highest sorting. | [optional] [readonly] 
**ObjectGroupTitle** | **string** | The name of the group. NULL if no group. | [optional] 
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
**AutoBudgetAmount** | **string** | The amount for the auto-budget, if set. | [optional] 
**PcAutoBudgetAmount** | **string** | The amount for the auto-budget, if set in the primary currency of the administration. | [optional] 
**Spent** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Information on how much was spent in this budget. Is only filled in when the start and end date are submitted. | [optional] [readonly] 
**PcSpent** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Information on how much was spent in this budget. Is only filled in when the start and end date are submitted. It is converted to the primary currency of the administration. | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

