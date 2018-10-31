# TripletexApi::EmployeeemploymentdetailsApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](EmployeeemploymentdetailsApi.md#get) | **GET** /employee/employment/details/{id} | [BETA] Find employment details by ID.
[**post**](EmployeeemploymentdetailsApi.md#post) | **POST** /employee/employment/details | [BETA] Create employment details.
[**put**](EmployeeemploymentdetailsApi.md#put) | **PUT** /employee/employment/details/{id} | [BETA] Update employment details. 
[**search**](EmployeeemploymentdetailsApi.md#search) | **GET** /employee/employment/details | [BETA] Find all employmentdetails for employment.


# **get**
> ResponseWrapperEmploymentDetails get(id, opts)

[BETA] Find employment details by ID.



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

api_instance = TripletexApi::EmployeeemploymentdetailsApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Find employment details by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling EmployeeemploymentdetailsApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperEmploymentDetails**](ResponseWrapperEmploymentDetails.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **post**
> ResponseWrapperEmploymentDetails post(opts)

[BETA] Create employment details.



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

api_instance = TripletexApi::EmployeeemploymentdetailsApi.new

opts = { 
  body: TripletexApi::EmploymentDetails.new # EmploymentDetails | JSON representing the new object to be created. Should not have ID and version set.
}

begin
  #[BETA] Create employment details.
  result = api_instance.post(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling EmployeeemploymentdetailsApi->post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**EmploymentDetails**](EmploymentDetails.md)| JSON representing the new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ResponseWrapperEmploymentDetails**](ResponseWrapperEmploymentDetails.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put**
> ResponseWrapperEmploymentDetails put(id, opts)

[BETA] Update employment details. 



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

api_instance = TripletexApi::EmployeeemploymentdetailsApi.new

id = 56 # Integer | Element ID

opts = { 
  body: TripletexApi::EmploymentDetails.new # EmploymentDetails | Partial object describing what should be updated
}

begin
  #[BETA] Update employment details. 
  result = api_instance.put(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling EmployeeemploymentdetailsApi->put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **body** | [**EmploymentDetails**](EmploymentDetails.md)| Partial object describing what should be updated | [optional] 

### Return type

[**ResponseWrapperEmploymentDetails**](ResponseWrapperEmploymentDetails.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **search**
> ListResponseEmploymentDetails search(opts)

[BETA] Find all employmentdetails for employment.



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

api_instance = TripletexApi::EmployeeemploymentdetailsApi.new

opts = { 
  employment_id: 56, # Integer | Element ID
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Find all employmentdetails for employment.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling EmployeeemploymentdetailsApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employment_id** | **Integer**| Element ID | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseEmploymentDetails**](ListResponseEmploymentDetails.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



