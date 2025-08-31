# Brotal.FireflyIII.Model.PiggyBankProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**CreatedAt** | **DateTime** |  | [optional] [readonly] 
**UpdatedAt** | **DateTime** |  | [optional] [readonly] 
**Percentage** | **decimal** | The percentage of the target amount that has been saved, if a target amount is set. | [optional] [readonly] 
**StartDate** | **DateTime** | The date you started with this piggy bank. | [optional] 
**TargetDate** | **DateTime** | The date you intend to finish saving money. | [optional] 
**Order** | **int** |  | [optional] 
**Active** | **bool** |  | [optional] [readonly] 
**Notes** | **string** |  | [optional] 
**ObjectGroupId** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] 
**ObjectGroupOrder** | **int** | The order of the group. At least 1, for the highest sorting. | [optional] [readonly] 
**ObjectGroupTitle** | **string** | The name of the group. NULL if no group. | [optional] 
**Accounts** | [**List&lt;PiggyBankAccountRead&gt;**](PiggyBankAccountRead.md) |  | [optional] 
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
**TargetAmount** | **string** |  | 
**PcTargetAmount** | **string** | The target amount in the primary currency of the administration. | [optional] 
**CurrentAmount** | **string** |  | [optional] 
**PcCurrentAmount** | **string** | The current amount in the primary currency of the administration. | [optional] 
**LeftToSave** | **string** |  | [optional] 
**PcLeftToSave** | **string** |  | [optional] 
**SavePerMonth** | **string** |  | [optional] [readonly] 
**PcSavePerMonth** | **string** |  | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

