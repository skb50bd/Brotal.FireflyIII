# Brotal.FireflyIII.Model.RecurrenceProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **DateTime** |  | [optional] [readonly] 
**UpdatedAt** | **DateTime** |  | [optional] [readonly] 
**Type** | **RecurrenceTransactionType** |  | [optional] 
**Title** | **string** |  | [optional] 
**Description** | **string** | Not to be confused with the description of the actual transaction(s) being created. | [optional] 
**FirstDate** | **DateOnly** | First time the recurring transaction will fire. Must be after today. | [optional] 
**LatestDate** | **DateOnly** | Last time the recurring transaction has fired. | [optional] [readonly] 
**RepeatUntil** | **DateOnly** | Date until the recurring transaction can fire. Use either this field or repetitions. | [optional] 
**ApplyRules** | **bool** | Whether or not to fire the rules after the creation of a transaction. | [optional] 
**Active** | **bool** | If the recurrence is even active. | [optional] 
**NrOfRepetitions** | **int** | Max number of created transactions. Use either this field or repeat_until. | [optional] 
**Notes** | **string** |  | [optional] 
**Repetitions** | [**List&lt;RecurrenceRepetition&gt;**](RecurrenceRepetition.md) |  | [optional] 
**Transactions** | [**List&lt;RecurrenceTransaction&gt;**](RecurrenceTransaction.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

