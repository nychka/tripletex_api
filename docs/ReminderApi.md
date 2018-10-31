# TripletexApi::ReminderApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](ReminderApi.md#get) | **GET** /reminder/{id} | Get reminder by ID.
[**search**](ReminderApi.md#search) | **GET** /reminder | Find reminders corresponding with sent data.


# **get**
> ResponseWrapperReminder get(id, opts)

Get reminder by ID.



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

api_instance = TripletexApi::ReminderApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Get reminder by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ReminderApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperReminder**](ResponseWrapperReminder.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **search**
> ListResponseReminder search(date_from, date_to, opts)

Find reminders corresponding with sent data.



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

api_instance = TripletexApi::ReminderApi.new

date_from = "date_from_example" # String | From and including

date_to = "date_to_example" # String | To and excluding

opts = { 
  id: "id_example", # String | List of IDs
  term_of_payment_to: "term_of_payment_to_example", # String | To and excluding
  term_of_payment_from: "term_of_payment_from_example", # String | From and including
  invoice_id: 56, # Integer | Equals
  customer_id: 56, # Integer | Equals
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find reminders corresponding with sent data.
  result = api_instance.search(date_from, date_to, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ReminderApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **date_from** | **String**| From and including | 
 **date_to** | **String**| To and excluding | 
 **id** | **String**| List of IDs | [optional] 
 **term_of_payment_to** | **String**| To and excluding | [optional] 
 **term_of_payment_from** | **String**| From and including | [optional] 
 **invoice_id** | **Integer**| Equals | [optional] 
 **customer_id** | **Integer**| Equals | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseReminder**](ListResponseReminder.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



