# TripletexApi::BankStatement

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **Integer** |  | [optional] 
**version** | **Integer** |  | [optional] 
**changes** | [**Array&lt;Change&gt;**](Change.md) |  | [optional] 
**url** | **String** |  | [optional] 
**balance_currency** | **Float** | Balance on the account. | [optional] 
**file_name** | **String** | Bank statement file name. | [optional] 
**bank** | [**Bank**](Bank.md) | Bank | [optional] 
**transactions** | [**Array&lt;BankTransaction&gt;**](BankTransaction.md) | Bank transactions tied to the bank statement | [optional] 

