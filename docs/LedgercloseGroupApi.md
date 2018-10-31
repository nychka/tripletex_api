# TripletexApi::LedgercloseGroupApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](LedgercloseGroupApi.md#get) | **GET** /ledger/closeGroup/{id} | Get close group by ID.
[**search**](LedgercloseGroupApi.md#search) | **GET** /ledger/closeGroup | Find close groups corresponding with sent data.


# **get**
> ResponseWrapperCloseGroup get(id, opts)

Get close group by ID.



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

api_instance = TripletexApi::LedgercloseGroupApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Get close group by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling LedgercloseGroupApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperCloseGroup**](ResponseWrapperCloseGroup.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **search**
> ListResponseCloseGroup search(date_from, date_to, opts)

Find close groups corresponding with sent data.



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

api_instance = TripletexApi::LedgercloseGroupApi.new

date_from = "date_from_example" # String | From and including

date_to = "date_to_example" # String | To and excluding

opts = { 
  id: "id_example", # String | List of IDs
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find close groups corresponding with sent data.
  result = api_instance.search(date_from, date_to, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling LedgercloseGroupApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **date_from** | **String**| From and including | 
 **date_to** | **String**| To and excluding | 
 **id** | **String**| List of IDs | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseCloseGroup**](ListResponseCloseGroup.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



