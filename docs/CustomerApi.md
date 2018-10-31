# TripletexApi::CustomerApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](CustomerApi.md#get) | **GET** /customer/{id} | Get customer by ID.
[**post**](CustomerApi.md#post) | **POST** /customer | Create customer. Related customer addresses may also be created.
[**post_list**](CustomerApi.md#post_list) | **POST** /customer/list | [BETA] Create multiple customers. Related supplier addresses may also be created.
[**put**](CustomerApi.md#put) | **PUT** /customer/{id} | Update customer. 
[**put_list**](CustomerApi.md#put_list) | **PUT** /customer/list | [BETA] Update multiple customers. Addresses can also be updated.
[**search**](CustomerApi.md#search) | **GET** /customer | Find customers corresponding with sent data.


# **get**
> ResponseWrapperCustomer get(id, opts)

Get customer by ID.



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

api_instance = TripletexApi::CustomerApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Get customer by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling CustomerApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperCustomer**](ResponseWrapperCustomer.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **post**
> ResponseWrapperCustomer post(opts)

Create customer. Related customer addresses may also be created.



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

api_instance = TripletexApi::CustomerApi.new

opts = { 
  body: TripletexApi::Customer.new # Customer | JSON representing the new object to be created. Should not have ID and version set.
}

begin
  #Create customer. Related customer addresses may also be created.
  result = api_instance.post(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling CustomerApi->post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Customer**](Customer.md)| JSON representing the new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ResponseWrapperCustomer**](ResponseWrapperCustomer.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **post_list**
> ListResponseCustomer post_list(opts)

[BETA] Create multiple customers. Related supplier addresses may also be created.



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

api_instance = TripletexApi::CustomerApi.new

opts = { 
  body: [TripletexApi::Customer.new] # Array<Customer> | JSON representing a list of new object to be created. Should not have ID and version set.
}

begin
  #[BETA] Create multiple customers. Related supplier addresses may also be created.
  result = api_instance.post_list(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling CustomerApi->post_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Array&lt;Customer&gt;**](Customer.md)| JSON representing a list of new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ListResponseCustomer**](ListResponseCustomer.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put**
> ResponseWrapperCustomer put(id, opts)

Update customer. 



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

api_instance = TripletexApi::CustomerApi.new

id = 56 # Integer | Element ID

opts = { 
  body: TripletexApi::Customer.new # Customer | Partial object describing what should be updated
}

begin
  #Update customer. 
  result = api_instance.put(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling CustomerApi->put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **body** | [**Customer**](Customer.md)| Partial object describing what should be updated | [optional] 

### Return type

[**ResponseWrapperCustomer**](ResponseWrapperCustomer.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put_list**
> ListResponseCustomer put_list(opts)

[BETA] Update multiple customers. Addresses can also be updated.



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

api_instance = TripletexApi::CustomerApi.new

opts = { 
  body: [TripletexApi::Customer.new] # Array<Customer> | JSON representing updates to object. Should have ID and version set.
}

begin
  #[BETA] Update multiple customers. Addresses can also be updated.
  result = api_instance.put_list(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling CustomerApi->put_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Array&lt;Customer&gt;**](Customer.md)| JSON representing updates to object. Should have ID and version set. | [optional] 

### Return type

[**ListResponseCustomer**](ListResponseCustomer.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **search**
> ListResponseCustomer search(opts)

Find customers corresponding with sent data.



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

api_instance = TripletexApi::CustomerApi.new

opts = { 
  id: "id_example", # String | List of IDs
  customer_account_number: "customer_account_number_example", # String | List of IDs
  organization_number: "organization_number_example", # String | Equals
  email: "email_example", # String | Equals
  invoice_email: "invoice_email_example", # String | Equals
  is_inactive: false, # BOOLEAN | Equals
  account_manager_id: "account_manager_id_example", # String | List of IDs
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find customers corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling CustomerApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| List of IDs | [optional] 
 **customer_account_number** | **String**| List of IDs | [optional] 
 **organization_number** | **String**| Equals | [optional] 
 **email** | **String**| Equals | [optional] 
 **invoice_email** | **String**| Equals | [optional] 
 **is_inactive** | **BOOLEAN**| Equals | [optional] [default to false]
 **account_manager_id** | **String**| List of IDs | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseCustomer**](ListResponseCustomer.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



