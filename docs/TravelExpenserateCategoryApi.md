# TripletexApi::TravelExpenserateCategoryApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get**](TravelExpenserateCategoryApi.md#get) | **GET** /travelExpense/rateCategory/{id} | [BETA] Get travel expense rate category by ID.
[**search**](TravelExpenserateCategoryApi.md#search) | **GET** /travelExpense/rateCategory | [BETA] Find rate categories corresponding with sent data.


# **get**
> ResponseWrapperTravelExpenseRateCategory get(id, opts)

[BETA] Get travel expense rate category by ID.



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

api_instance = TripletexApi::TravelExpenserateCategoryApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Get travel expense rate category by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpenserateCategoryApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperTravelExpenseRateCategory**](ResponseWrapperTravelExpenseRateCategory.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **search**
> ListResponseTravelExpenseRateCategory search(opts)

[BETA] Find rate categories corresponding with sent data.



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

api_instance = TripletexApi::TravelExpenserateCategoryApi.new

opts = { 
  type: "type_example", # String | Equals
  name: "name_example", # String | Containing
  travel_report_rate_category_group_id: 56, # Integer | Equals
  amelding_wage_code: "amelding_wage_code_example", # String | Containing
  wage_code_number: "wage_code_number_example", # String | Equals
  is_valid_day_trip: true, # BOOLEAN | Equals
  is_valid_accommodation: true, # BOOLEAN | Equals
  is_valid_domestic: true, # BOOLEAN | Equals
  requires_zone: true, # BOOLEAN | Equals
  is_requires_overnight_accommodation: true, # BOOLEAN | Equals
  date_from: "date_from_example", # String | From and including
  date_to: "date_to_example", # String | To and excluding
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #[BETA] Find rate categories corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TravelExpenserateCategoryApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **type** | **String**| Equals | [optional] 
 **name** | **String**| Containing | [optional] 
 **travel_report_rate_category_group_id** | **Integer**| Equals | [optional] 
 **amelding_wage_code** | **String**| Containing | [optional] 
 **wage_code_number** | **String**| Equals | [optional] 
 **is_valid_day_trip** | **BOOLEAN**| Equals | [optional] 
 **is_valid_accommodation** | **BOOLEAN**| Equals | [optional] 
 **is_valid_domestic** | **BOOLEAN**| Equals | [optional] 
 **requires_zone** | **BOOLEAN**| Equals | [optional] 
 **is_requires_overnight_accommodation** | **BOOLEAN**| Equals | [optional] 
 **date_from** | **String**| From and including | [optional] 
 **date_to** | **String**| To and excluding | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseTravelExpenseRateCategory**](ListResponseTravelExpenseRateCategory.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



