# TripletexApi::LedgeraccountingPeriodApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](LedgeraccountingPeriodApi.md#get) | **GET** /ledger/accountingPeriod/{id} | Get accounting period by ID.
[**search**](LedgeraccountingPeriodApi.md#search) | **GET** /ledger/accountingPeriod | Find accounting periods corresponding with sent data.


# **get**
> ResponseWrapperAccountingPeriod get(id, opts)

Get accounting period by ID.



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

api_instance = TripletexApi::LedgeraccountingPeriodApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Get accounting period by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling LedgeraccountingPeriodApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperAccountingPeriod**](ResponseWrapperAccountingPeriod.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **search**
> ListResponseAccountingPeriod search(opts)

Find accounting periods corresponding with sent data.



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

api_instance = TripletexApi::LedgeraccountingPeriodApi.new

opts = { 
  id: "id_example", # String | List of IDs
  number_from: 56, # Integer | From and including
  number_to: 56, # Integer | To and excluding
  start_from: "start_from_example", # String | From and including
  start_to: "start_to_example", # String | To and excluding
  end_from: "end_from_example", # String | From and including
  end_to: "end_to_example", # String | To and excluding
  count: 1400, # Integer | Number of elements to return
  from: 0, # Integer | From index
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find accounting periods corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling LedgeraccountingPeriodApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| List of IDs | [optional] 
 **number_from** | **Integer**| From and including | [optional] 
 **number_to** | **Integer**| To and excluding | [optional] 
 **start_from** | **String**| From and including | [optional] 
 **start_to** | **String**| To and excluding | [optional] 
 **end_from** | **String**| From and including | [optional] 
 **end_to** | **String**| To and excluding | [optional] 
 **count** | **Integer**| Number of elements to return | [optional] [default to 1400]
 **from** | **Integer**| From index | [optional] [default to 0]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseAccountingPeriod**](ListResponseAccountingPeriod.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



