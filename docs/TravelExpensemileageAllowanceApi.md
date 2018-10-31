# TripletexApi::TravelExpensemileageAllowanceApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete**](TravelExpensemileageAllowanceApi.md#delete) | **DELETE** /travelExpense/mileageAllowance/{id} | [BETA] Delete mileage allowance.
[**get**](TravelExpensemileageAllowanceApi.md#get) | **GET** /travelExpense/mileageAllowance/{id} | [BETA] Get mileage allowance by ID.
[**post**](TravelExpensemileageAllowanceApi.md#post) | **POST** /travelExpense/mileageAllowance | [BETA] Create mileage allowance.
[**put**](TravelExpensemileageAllowanceApi.md#put) | **PUT** /travelExpense/mileageAllowance/{id} | [BETA] Update mileage allowance.
[**search**](TravelExpensemileageAllowanceApi.md#search) | **GET** /travelExpense/mileageAllowance | [BETA] Find mileage allowances corresponding with sent data.


# **delete**
> delete(id)

[BETA] Delete mileage allowance.



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

api_instance = TripletexApi::TravelExpensemileageAllowanceApi.new

id = 56 # Integer | Element ID


begin
  #[BETA] Delete mileage allowance.
  api_instance.delete(id)
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensemileageAllowanceApi->delete: #{e}"
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
> ResponseWrapperMileageAllowance get(id, opts)

[BETA] Get mileage allowance by ID.



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

api_instance = TripletexApi::TravelExpensemileageAllowanceApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Get mileage allowance by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensemileageAllowanceApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperMileageAllowance**](ResponseWrapperMileageAllowance.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **post**
> ResponseWrapperMileageAllowance post(opts)

[BETA] Create mileage allowance.



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

api_instance = TripletexApi::TravelExpensemileageAllowanceApi.new

opts = { 
  body: TripletexApi::MileageAllowance.new # MileageAllowance | JSON representing the new object to be created. Should not have ID and version set.
}

begin
  #[BETA] Create mileage allowance.
  result = api_instance.post(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensemileageAllowanceApi->post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**MileageAllowance**](MileageAllowance.md)| JSON representing the new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ResponseWrapperMileageAllowance**](ResponseWrapperMileageAllowance.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put**
> ResponseWrapperMileageAllowance put(id, opts)

[BETA] Update mileage allowance.



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

api_instance = TripletexApi::TravelExpensemileageAllowanceApi.new

id = 56 # Integer | Element ID

opts = { 
  body: TripletexApi::MileageAllowance.new # MileageAllowance | Partial object describing what should be updated
}

begin
  #[BETA] Update mileage allowance.
  result = api_instance.put(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensemileageAllowanceApi->put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **body** | [**MileageAllowance**](MileageAllowance.md)| Partial object describing what should be updated | [optional] 

### Return type

[**ResponseWrapperMileageAllowance**](ResponseWrapperMileageAllowance.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **search**
> ListResponseMileageAllowance search(opts)

[BETA] Find mileage allowances corresponding with sent data.



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

api_instance = TripletexApi::TravelExpensemileageAllowanceApi.new

opts = { 
  travel_expense_id: "travel_expense_id_example", # String | Equals
  rate_type_id: "rate_type_id_example", # String | Equals
  rate_category_id: "rate_category_id_example", # String | Equals
  km_from: 8.14, # Float | From and including
  km_to: 8.14, # Float | To and excluding
  rate_from: 8.14, # Float | From and including
  rate_to: 8.14, # Float | To and excluding
  amount_from: 8.14, # Float | From and including
  amount_to: 8.14, # Float | To and excluding
  departure_location: "departure_location_example", # String | Containing
  destination: "destination_example", # String | Containing
  date_from: "date_from_example", # String | From and including
  date_to: "date_to_example", # String | To and excluding
  is_company_car: true, # BOOLEAN | Equals
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Find mileage allowances corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpensemileageAllowanceApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **travel_expense_id** | **String**| Equals | [optional] 
 **rate_type_id** | **String**| Equals | [optional] 
 **rate_category_id** | **String**| Equals | [optional] 
 **km_from** | **Float**| From and including | [optional] 
 **km_to** | **Float**| To and excluding | [optional] 
 **rate_from** | **Float**| From and including | [optional] 
 **rate_to** | **Float**| To and excluding | [optional] 
 **amount_from** | **Float**| From and including | [optional] 
 **amount_to** | **Float**| To and excluding | [optional] 
 **departure_location** | **String**| Containing | [optional] 
 **destination** | **String**| Containing | [optional] 
 **date_from** | **String**| From and including | [optional] 
 **date_to** | **String**| To and excluding | [optional] 
 **is_company_car** | **BOOLEAN**| Equals | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseMileageAllowance**](ListResponseMileageAllowance.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



