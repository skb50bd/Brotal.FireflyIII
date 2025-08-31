# Brotal.FireflyIII.Model.CategoryProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**CreatedAt** | **DateTime** |  | [optional] [readonly] 
**UpdatedAt** | **DateTime** |  | [optional] [readonly] 
**Notes** | **string** |  | [optional] 
**ObjectHasCurrencySetting** | **bool** | This object never has its own currency setting, so this value is always false. | [optional] 
**PrimaryCurrencyId** | **string** | The currency ID of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencyName** | **string** | The currency name of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencyCode** | **string** | The currency code of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencySymbol** | **string** | The currency symbol of the administration&#39;s primary currency. | [optional] [readonly] 
**PrimaryCurrencyDecimalPlaces** | **int** | The currency decimal places of the administration&#39;s primary currency. | [optional] [readonly] 
**Spent** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Amount(s) spent in the currencies in the database for this category. ONLY present when start and date are set. | [optional] [readonly] 
**PcSpent** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Amount(s) spent in the primary currency in the database for this category. ONLY present when start and date are set.  | [optional] [readonly] 
**Earned** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Amount(s) earned in the currencies in the database for this category. ONLY present when start and date are set. | [optional] [readonly] 
**PcEarned** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Amount(s) earned in the primary currency in the database for this category. ONLY present when start and date are set.  | [optional] [readonly] 
**Transferred** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Amount(s) transferred in the currencies in the database for this category. ONLY present when start and date are set.  | [optional] [readonly] 
**PcTransferred** | [**List&lt;ArrayEntryWithCurrencyAndSum&gt;**](ArrayEntryWithCurrencyAndSum.md) | Amount(s) transferred in primary currency in the database for this category. ONLY present when start and date are set.  | [optional] [readonly] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

