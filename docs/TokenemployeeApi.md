# TripletexApi::TokenemployeeApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create**](TokenemployeeApi.md#create) | **PUT** /token/employee/:create | Create an employee token. Only selected consumers are allowed


# **create**
> ResponseWrapperEmployeeToken create(token_name, consumer_name, employee_id, company_owned, expiration_date)

Create an employee token. Only selected consumers are allowed



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

api_instance = TripletexApi::TokenemployeeApi.new

token_name = "token_name_example" # String | A user defined name for the new token

consumer_name = "consumer_name_example" # String | The name of the consumer

employee_id = 56 # Integer | The id of the employee

company_owned = true # BOOLEAN | Is the key company owned

expiration_date = "expiration_date_example" # String | Expiration date for the employeeToken


begin
  #Create an employee token. Only selected consumers are allowed
  result = api_instance.create(token_name, consumer_name, employee_id, company_owned, expiration_date)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TokenemployeeApi->create: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token_name** | **String**| A user defined name for the new token | 
 **consumer_name** | **String**| The name of the consumer | 
 **employee_id** | **Integer**| The id of the employee | 
 **company_owned** | **BOOLEAN**| Is the key company owned | 
 **expiration_date** | **String**| Expiration date for the employeeToken | 

### Return type

[**ResponseWrapperEmployeeToken**](ResponseWrapperEmployeeToken.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



