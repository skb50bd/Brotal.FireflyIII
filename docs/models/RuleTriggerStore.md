# Brotal.FireflyIII.Model.RuleTriggerStore

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **RuleTriggerKeyword** |  | 
**Value** | **string** | The accompanying value the trigger responds to. This value is often mandatory, but this depends on the trigger. | 
**Order** | **int** | Order of the trigger | [optional] 
**Active** | **bool** | If the trigger is active. Defaults to true. | [optional] [default to true]
**Prohibited** | **bool** | If &#39;prohibited&#39; is true, this rule trigger will be negated. &#39;Description is&#39; will become &#39;Description is NOT&#39; etc. | [optional] [default to false]
**StopProcessing** | **bool** | When true, other triggers will not be checked if this trigger was triggered. Defaults to false. | [optional] [default to false]

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

