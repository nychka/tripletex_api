# TripletexApi::BankstatementtransactionApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](BankstatementtransactionApi.md#get) | **GET** /bank/statement/transaction/{id} | [BETA] Get bank transaction by ID.
[**get_details**](BankstatementtransactionApi.md#get_details) | **GET** /bank/statement/transaction/{id}/details | [BETA] Get additional details about transaction by ID.
[**search**](BankstatementtransactionApi.md#search) | **GET** /bank/statement/transaction | [BETA] Find bank transaction corresponding with sent data.


# **get**
> ResponseWrapperBankTransaction get(id, opts)

[BETA] Get bank transaction by ID.



### Example
```ruby
# load the gem
require 'tripletex_api'
# setup authorization
TripletexApi.configure do |config|
  # Configure HTTP basic authorization: tokenAuthScheme
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = TripletexApi::BankstatementtransactionApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Get bank transaction by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling BankstatementtransactionApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperBankTransaction**](ResponseWrapperBankTransaction.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **get_details**
> ResponseWrapperObject get_details(id, opts)

[BETA] Get additional details about transaction by ID.



### Example
```ruby
# load the gem
require 'tripletex_api'
# setup authorization
TripletexApi.configure do |config|
  # Configure HTTP basic authorization: tokenAuthScheme
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = TripletexApi::BankstatementtransactionApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Get additional details about transaction by ID.
  result = api_instance.get_details(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling BankstatementtransactionApi->get_details: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperObject**](ResponseWrapperObject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json



# **search**
> ListResponseBankTransaction search(bank_statement_id, opts)

[BETA] Find bank transaction corresponding with sent data.



### Example
```ruby
# load the gem
require 'tripletex_api'
# setup authorization
TripletexApi.configure do |config|
  # Configure HTTP basic authorization: tokenAuthScheme
  config.username = 'YOUR USERNAME'
  config.password = 'YOUR PASSWORD'
end

api_instance = TripletexApi::BankstatementtransactionApi.new

bank_statement_id = 56 # Integer | Bank statement ID

opts = { 
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Find bank transaction corresponding with sent data.
  result = api_instance.search(bank_statement_id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling BankstatementtransactionApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bank_statement_id** | **Integer**| Bank statement ID | 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseBankTransaction**](ListResponseBankTransaction.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



