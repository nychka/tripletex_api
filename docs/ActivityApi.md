# TripletexApi::ActivityApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](ActivityApi.md#get) | **GET** /activity/{id} | Find activity by ID.
[**get_for_time_sheet**](ActivityApi.md#get_for_time_sheet) | **GET** /activity/&gt;forTimeSheet | Find applicable time sheet activities for an employee on a specific day.
[**search**](ActivityApi.md#search) | **GET** /activity | Find activities corresponding with sent data.


# **get**
> ResponseWrapperActivity get(id, opts)

Find activity by ID.



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

api_instance = TripletexApi::ActivityApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find activity by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ActivityApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperActivity**](ResponseWrapperActivity.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **get_for_time_sheet**
> ListResponseActivity get_for_time_sheet(project_id, opts)

Find applicable time sheet activities for an employee on a specific day.



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

api_instance = TripletexApi::ActivityApi.new

project_id = 56 # Integer | Project ID

opts = { 
  employee_id: 56, # Integer | Employee ID. Defaults to ID of token owner.
  date: "date_example", # String | yyyy-MM-dd. Defaults to today.
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find applicable time sheet activities for an employee on a specific day.
  result = api_instance.get_for_time_sheet(project_id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ActivityApi->get_for_time_sheet: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **Integer**| Project ID | 
 **employee_id** | **Integer**| Employee ID. Defaults to ID of token owner. | [optional] 
 **date** | **String**| yyyy-MM-dd. Defaults to today. | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseActivity**](ListResponseActivity.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **search**
> ListResponseActivity search(opts)

Find activities corresponding with sent data.



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

api_instance = TripletexApi::ActivityApi.new

opts = { 
  id: "id_example", # String | List of IDs
  name: "name_example", # String | Containing
  number: "number_example", # String | Equals
  description: "description_example", # String | Containing
  is_project_activity: true, # BOOLEAN | Equals
  is_general: true, # BOOLEAN | Equals
  is_chargeable: true, # BOOLEAN | Equals
  is_task: true, # BOOLEAN | Equals
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find activities corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ActivityApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| List of IDs | [optional] 
 **name** | **String**| Containing | [optional] 
 **number** | **String**| Equals | [optional] 
 **description** | **String**| Containing | [optional] 
 **is_project_activity** | **BOOLEAN**| Equals | [optional] 
 **is_general** | **BOOLEAN**| Equals | [optional] 
 **is_chargeable** | **BOOLEAN**| Equals | [optional] 
 **is_task** | **BOOLEAN**| Equals | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseActivity**](ListResponseActivity.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



