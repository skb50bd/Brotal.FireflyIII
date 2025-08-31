# Brotal.FireflyIII.Model.ChartDataSet

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Label** | **string** | This is the title of the current set. It can refer to an account, a budget or another object (by name). | [optional] 
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
**Date** | **DateTime** |  | [optional] 
**StartDate** | **DateTime** |  | [optional] 
**EndDate** | **DateTime** |  | [optional] 
**Type** | **string** | Indicated the type of chart that is expected to be rendered. You can safely ignore this if you want. | [optional] 
**Period** | **ChartDatasetPeriodProperty** |  | [optional] 
**YAxisID** | **int** | Used to indicate the Y axis for this data set. Is usually between 0 and 1 (left and right side of the chart). | [optional] 
**Entries** | [**List&lt;ChartDataPoint&gt;**](ChartDataPoint.md) | The actual entries for this data set. They &#39;key&#39; value is the label for the data point. The value is the actual (numerical) value. | [optional] 
**PcEntries** | [**List&lt;ChartDataPoint&gt;**](ChartDataPoint.md) | The actual entries for this data set. They &#39;key&#39; value is the label for the data point. The value is the actual (numerical) value. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

