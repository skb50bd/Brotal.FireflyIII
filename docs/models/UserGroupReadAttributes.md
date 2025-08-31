# Brotal.FireflyIII.Model.UserGroupReadAttributes

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **DateTime** |  | [optional] [readonly] 
**UpdatedAt** | **DateTime** |  | [optional] [readonly] 
**InUse** | **bool** | Is this user group (&#39;financial administration&#39;) currently the active administration? | [optional] [readonly] 
**CanSeeMembers** | **bool** | Can the current user see the members of this user group? | [optional] [readonly] 
**Title** | **string** | Title of the user group. By default, it is the same as the user&#39;s email address. | [optional] 
**PrimaryCurrencyId** | **string** | Returns the primary currency ID of the user group. | [optional] [readonly] 
**PrimaryCurrencyCode** | **string** | Returns the primary currency code of the user group. | [optional] 
**PrimaryCurrencySymbol** | **string** | Returns the primary currency symbol of the user group. | [optional] [readonly] 
**PrimaryCurrencyDecimalPlaces** | **int** | Returns the primary currency decimal places of the user group. | [optional] [readonly] 
**Members** | [**List&lt;UserGroupReadMembers&gt;**](UserGroupReadMembers.md) |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

