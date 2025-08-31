# Brotal.FireflyIII.Model.AccountProperties

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **string** |  | 
**Type** | **ShortAccountTypeProperty** |  | 
**CreatedAt** | **DateTime** |  | [optional] [readonly] 
**UpdatedAt** | **DateTime** |  | [optional] [readonly] 
**Active** | **bool** |  | [optional] [default to true]
**Order** | **int** | Order of the account. Is NULL if account is not asset or liability. | [optional] 
**AccountRole** | **AccountRoleProperty** |  | [optional] 
**ObjectGroupId** | **string** | The group ID of the group this object is part of. NULL if no group. | [optional] 
**ObjectGroupOrder** | **int** | The order of the group. At least 1, for the highest sorting. | [optional] [readonly] 
**ObjectGroupTitle** | **string** | The name of the group. NULL if no group. | [optional] 
**ObjectHasCurrencySetting** | **bool** | Indicates whether the account has a currency setting. If false, the account uses the administration&#39;s primary currency. Asset accounts and liability accounts always have a currency setting, while expense and revenue accounts do not. | [optional] [readonly] 
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
**CurrentBalance** | **string** | The current balance of the account in the account&#39;s currency. If the account has no currency, this is the balance in the administration&#39;s primary currency. Either way, the &#x60;currency_*&#x60; fields reflect the currency used. | [optional] [readonly] 
**PcCurrentBalance** | **string** | The current balance of the account in the administration&#39;s primary currency. The &#x60;primary_currency_*&#x60; fields reflect the currency used. This field is NULL if the user does have &#39;convert to primary&#39; set to true in their settings. | [optional] [readonly] 
**OpeningBalance** | **string** | Represents the opening balance, the initial amount this account holds in the currency of the account or the administration&#39;s primary currency if the account has no currency. Either way, the &#x60;currency_*&#x60; fields reflect the currency used. | [optional] 
**PcOpeningBalance** | **string** | The opening balance of the account in the administration&#39;s primary currency (pc). The &#x60;primary_currency_*&#x60; fields reflect the currency used. This field is NULL if the user does have &#39;convert to primary&#39; set to true in their settings. | [optional] 
**VirtualBalance** | **string** | The virtual balance of the account in the account&#39;s currency or the administration&#39;s primary currency if the account has no currency. | [optional] 
**PcVirtualBalance** | **string** | The virtual balance of the account in the administration&#39;s primary currency (pc). The &#x60;primary_currency_*&#x60; fields reflect the currency used. This field is NULL if the user does have &#39;convert to primary&#39; set to true in their settings. | [optional] 
**DebtAmount** | **string** | In liability accounts (loans, debts and mortgages), this is the amount of debt in the account&#39;s currency (see the &#x60;currency_*&#x60; fields). In asset accounts, this is NULL. | [optional] 
**PcDebtAmount** | **string** | In liability accounts (loans, debts and mortgages), this is the amount of debt in the administration&#39;s primary currency (see the &#x60;currency_*&#x60; fields. In asset accounts, this is NULL. | [optional] 
**CurrentBalanceDate** | **DateTime** | The timestamp for this date is always 23:59:59, to indicate it&#39;s the balance at the very END of that particular day. | [optional] [readonly] 
**Notes** | **string** |  | [optional] 
**MonthlyPaymentDate** | **DateTime** | Mandatory when the account_role is ccAsset. Moment at which CC payment installments are asked for by the bank. | [optional] 
**CreditCardType** | **CreditCardTypeProperty** |  | [optional] 
**AccountNumber** | **string** |  | [optional] 
**Iban** | **string** |  | [optional] 
**Bic** | **string** |  | [optional] 
**OpeningBalanceDate** | **DateTime** | Represents the date of the opening balance. | [optional] 
**LiabilityType** | **LiabilityTypeProperty** |  | [optional] 
**LiabilityDirection** | **LiabilityDirectionProperty** |  | [optional] 
**Interest** | **string** | Mandatory when type is liability. Interest percentage. | [optional] 
**InterestPeriod** | **InterestPeriodProperty** |  | [optional] 
**IncludeNetWorth** | **bool** |  | [optional] [default to true]
**Longitude** | **double** | Latitude of the accounts&#39;s location, if applicable. Can be used to draw a map. | [optional] 
**Latitude** | **double** | Latitude of the accounts&#39;s location, if applicable. Can be used to draw a map. | [optional] 
**ZoomLevel** | **int** | Zoom level for the map, if drawn. This to set the box right. Unfortunately this is a proprietary value because each map provider has different zoom levels. | [optional] 
**LastActivity** | **DateTime** | Last activity of the account. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

