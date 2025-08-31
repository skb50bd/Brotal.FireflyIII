# Brotal.FireflyIII.Model.RecurrenceStore

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **RecurrenceTransactionType** |  | 
**Title** | **string** |  | 
**FirstDate** | **DateOnly** | First time the recurring transaction will fire. Must be after today. | 
**Repetitions** | [**List&lt;RecurrenceRepetitionStore&gt;**](RecurrenceRepetitionStore.md) |  | 
**Transactions** | [**List&lt;RecurrenceTransactionStore&gt;**](RecurrenceTransactionStore.md) |  | 
**Description** | **string** | Not to be confused with the description of the actual transaction(s) being created. | [optional] 
**RepeatUntil** | **DateOnly** | Date until the recurring transaction can fire. Use either this field or repetitions. | 
**NrOfRepetitions** | **int** | Max number of created transactions. Use either this field or repeat_until. | [optional] 
**ApplyRules** | **bool** | Whether or not to fire the rules after the creation of a transaction. | [optional] 
**Active** | **bool** | If the recurrence is even active. | [optional] 
**Notes** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

