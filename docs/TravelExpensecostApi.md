# TripletexApi::TravelExpensecostApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete**](TravelExpensecostApi.md#delete) | **DELETE** /travelExpense/cost/{id} | [BETA] Delete cost.
[**get**](TravelExpensecostApi.md#get) | **GET** /travelExpense/cost/{id} | [BETA] Get cost by ID.
[**post**](TravelExpensecostApi.md#post) | **POST** /travelExpense/cost | [BETA] Create cost.
[**put**](TravelExpensecostApi.md#put) | **PUT** /travelExpense/cost/{id} | [BETA] Update cost.
[**search**](TravelExpensecostApi.md#search) | **GET** /travelExpense/cost | [BETA] Find costs corresponding with sent data.


# **delete**
> delete(id)

[BETA] Delete cost.



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

api_instance = TripletexApi::TravelExpensecostApi.new

id = 56 # Integer | Element ID


begin
  #[BETA] Delete cost.
  api_instance.delete(id)
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensecostApi->delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 

### Return type

nil (empty response body)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **get**
> ResponseWrapperCost get(id, opts)

[BETA] Get cost by ID.



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

api_instance = TripletexApi::TravelExpensecostApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Get cost by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensecostApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperCost**](ResponseWrapperCost.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **post**
> ResponseWrapperCost post(opts)

[BETA] Create cost.



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

api_instance = TripletexApi::TravelExpensecostApi.new

opts = { 
  body: TripletexApi::Cost.new # Cost | JSON representing the new object to be created. Should not have ID and version set.
}

begin
  #[BETA] Create cost.
  result = api_instance.post(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensecostApi->post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Cost**](Cost.md)| JSON representing the new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ResponseWrapperCost**](ResponseWrapperCost.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put**
> ResponseWrapperCost put(id, opts)

[BETA] Update cost.



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

api_instance = TripletexApi::TravelExpensecostApi.new

id = 56 # Integer | Element ID

opts = { 
  body: TripletexApi::Cost.new # Cost | Partial object describing what should be updated
}

begin
  #[BETA] Update cost.
  result = api_instance.put(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensecostApi->put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **body** | [**Cost**](Cost.md)| Partial object describing what should be updated | [optional] 

### Return type

[**ResponseWrapperCost**](ResponseWrapperCost.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **search**
> ListResponseCost search(opts)

[BETA] Find costs corresponding with sent data.



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

api_instance = TripletexApi::TravelExpensecostApi.new

opts = { 
  travel_expense_id: "travel_expense_id_example", # String | Equals
  vat_type_id: "vat_type_id_example", # String | Equals
  currency_id: "currency_id_example", # String | Equals
  rate_from: 8.14, # Float | From and including
  rate_to: 8.14, # Float | To and excluding
  count_from: 56, # Integer | From and including
  count_to: 56, # Integer | To and excluding
  amount_from: 8.14, # Float | From and including
  amount_to: 8.14, # Float | To and excluding
  location: "location_example", # String | Containing
  address: "address_example", # String | Containing
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Find costs corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensecostApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **travel_expense_id** | **String**| Equals | [optional] 
 **vat_type_id** | **String**| Equals | [optional] 
 **currency_id** | **String**| Equals | [optional] 
 **rate_from** | **Float**| From and including | [optional] 
 **rate_to** | **Float**| To and excluding | [optional] 
 **count_from** | **Integer**| From and including | [optional] 
 **count_to** | **Integer**| To and excluding | [optional] 
 **amount_from** | **Float**| From and including | [optional] 
 **amount_to** | **Float**| To and excluding | [optional] 
 **location** | **String**| Containing | [optional] 
 **address** | **String**| Containing | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseCost**](ListResponseCost.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



