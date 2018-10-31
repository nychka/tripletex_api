# TripletexApi::TravelExpenseperDiemCompensationApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete**](TravelExpenseperDiemCompensationApi.md#delete) | **DELETE** /travelExpense/perDiemCompensation/{id} | [BETA] Delete per diem compensation.
[**get**](TravelExpenseperDiemCompensationApi.md#get) | **GET** /travelExpense/perDiemCompensation/{id} | [BETA] Get per diem compensation by ID.
[**post**](TravelExpenseperDiemCompensationApi.md#post) | **POST** /travelExpense/perDiemCompensation | [BETA] Create per diem compensation.
[**put**](TravelExpenseperDiemCompensationApi.md#put) | **PUT** /travelExpense/perDiemCompensation/{id} | [BETA] Update per diem compensation.
[**search**](TravelExpenseperDiemCompensationApi.md#search) | **GET** /travelExpense/perDiemCompensation | [BETA] Find per diem compensations corresponding with sent data.


# **delete**
> delete(id)

[BETA] Delete per diem compensation.



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

api_instance = TripletexApi::TravelExpenseperDiemCompensationApi.new

id = 56 # Integer | Element ID


begin
  #[BETA] Delete per diem compensation.
  api_instance.delete(id)
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpenseperDiemCompensationApi->delete: #{e}"
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
> ResponseWrapperPerDiemCompensation get(id, opts)

[BETA] Get per diem compensation by ID.



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

api_instance = TripletexApi::TravelExpenseperDiemCompensationApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Get per diem compensation by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpenseperDiemCompensationApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperPerDiemCompensation**](ResponseWrapperPerDiemCompensation.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **post**
> ResponseWrapperPerDiemCompensation post(opts)

[BETA] Create per diem compensation.



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

api_instance = TripletexApi::TravelExpenseperDiemCompensationApi.new

opts = { 
  body: TripletexApi::PerDiemCompensation.new # PerDiemCompensation | JSON representing the new object to be created. Should not have ID and version set.
}

begin
  #[BETA] Create per diem compensation.
  result = api_instance.post(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpenseperDiemCompensationApi->post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PerDiemCompensation**](PerDiemCompensation.md)| JSON representing the new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ResponseWrapperPerDiemCompensation**](ResponseWrapperPerDiemCompensation.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put**
> ResponseWrapperPerDiemCompensation put(id, opts)

[BETA] Update per diem compensation.



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

api_instance = TripletexApi::TravelExpenseperDiemCompensationApi.new

id = 56 # Integer | Element ID

opts = { 
  body: TripletexApi::PerDiemCompensation.new # PerDiemCompensation | Partial object describing what should be updated
}

begin
  #[BETA] Update per diem compensation.
  result = api_instance.put(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpenseperDiemCompensationApi->put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **body** | [**PerDiemCompensation**](PerDiemCompensation.md)| Partial object describing what should be updated | [optional] 

### Return type

[**ResponseWrapperPerDiemCompensation**](ResponseWrapperPerDiemCompensation.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **search**
> ListResponsePerDiemCompensation search(opts)

[BETA] Find per diem compensations corresponding with sent data.



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

api_instance = TripletexApi::TravelExpenseperDiemCompensationApi.new

opts = { 
  travel_expense_id: "travel_expense_id_example", # String | Equals
  rate_type_id: "rate_type_id_example", # String | Equals
  rate_category_id: "rate_category_id_example", # String | Equals
  overnight_accommodation: "overnight_accommodation_example", # String | Equals
  count_from: 56, # Integer | From and including
  count_to: 56, # Integer | To and excluding
  rate_from: 8.14, # Float | From and including
  rate_to: 8.14, # Float | To and excluding
  amount_from: 8.14, # Float | From and including
  amount_to: 8.14, # Float | To and excluding
  location: "location_example", # String | Containing
  address: "address_example", # String | Containing
  is_deduction_for_breakfast: true, # BOOLEAN | Equals
  is_lunch_deduction: true, # BOOLEAN | Equals
  is_dinner_deduction: true, # BOOLEAN | Equals
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Find per diem compensations corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpenseperDiemCompensationApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **travel_expense_id** | **String**| Equals | [optional] 
 **rate_type_id** | **String**| Equals | [optional] 
 **rate_category_id** | **String**| Equals | [optional] 
 **overnight_accommodation** | **String**| Equals | [optional] 
 **count_from** | **Integer**| From and including | [optional] 
 **count_to** | **Integer**| To and excluding | [optional] 
 **rate_from** | **Float**| From and including | [optional] 
 **rate_to** | **Float**| To and excluding | [optional] 
 **amount_from** | **Float**| From and including | [optional] 
 **amount_to** | **Float**| To and excluding | [optional] 
 **location** | **String**| Containing | [optional] 
 **address** | **String**| Containing | [optional] 
 **is_deduction_for_breakfast** | **BOOLEAN**| Equals | [optional] 
 **is_lunch_deduction** | **BOOLEAN**| Equals | [optional] 
 **is_dinner_deduction** | **BOOLEAN**| Equals | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponsePerDiemCompensation**](ListResponsePerDiemCompensation.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



