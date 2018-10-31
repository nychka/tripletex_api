# TripletexApi::ProjectApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete**](ProjectApi.md#delete) | **DELETE** /project/{id} | [BETA] Delete project.
[**delete_by_ids**](ProjectApi.md#delete_by_ids) | **DELETE** /project/list | [BETA] Delete projects.
[**delete_list**](ProjectApi.md#delete_list) | **DELETE** /project | [BETA] Delete multiple projects.
[**get**](ProjectApi.md#get) | **GET** /project/{id} | Find project by ID.
[**get_for_time_sheet**](ProjectApi.md#get_for_time_sheet) | **GET** /project/&gt;forTimeSheet | Find projects applicable for time sheet registration on a specific day.
[**post**](ProjectApi.md#post) | **POST** /project | [BETA] Add new project.
[**post_list**](ProjectApi.md#post_list) | **POST** /project/list | [BETA] Register new projects. Multiple projects for different users can be sent in the same request.
[**put**](ProjectApi.md#put) | **PUT** /project/{id} | [BETA] Update project.
[**put_list**](ProjectApi.md#put_list) | **PUT** /project/list | [BETA] Update multiple projects.
[**search**](ProjectApi.md#search) | **GET** /project | Find projects corresponding with sent data.


# **delete**
> delete(id)

[BETA] Delete project.



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

api_instance = TripletexApi::ProjectApi.new

id = 56 # Integer | Element ID


begin
  #[BETA] Delete project.
  api_instance.delete(id)
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->delete: #{e}"
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



# **delete_by_ids**
> delete_by_ids(ids)

[BETA] Delete projects.



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

api_instance = TripletexApi::ProjectApi.new

ids = "ids_example" # String | ID of the elements


begin
  #[BETA] Delete projects.
  api_instance.delete_by_ids(ids)
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->delete_by_ids: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ids** | **String**| ID of the elements | 

### Return type

nil (empty response body)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **delete_list**
> delete_list(opts)

[BETA] Delete multiple projects.



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

api_instance = TripletexApi::ProjectApi.new

opts = { 
  body: [TripletexApi::Project.new] # Array<Project> | JSON representing objects to delete. Should have ID and version set.
}

begin
  #[BETA] Delete multiple projects.
  api_instance.delete_list(opts)
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->delete_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Array&lt;Project&gt;**](Project.md)| JSON representing objects to delete. Should have ID and version set. | [optional] 

### Return type

nil (empty response body)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **get**
> ResponseWrapperProject get(id, opts)

Find project by ID.



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

api_instance = TripletexApi::ProjectApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find project by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperProject**](ResponseWrapperProject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **get_for_time_sheet**
> ListResponseProject get_for_time_sheet(opts)

Find projects applicable for time sheet registration on a specific day.



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

api_instance = TripletexApi::ProjectApi.new

opts = { 
  employee_id: 56, # Integer | Employee ID. Defaults to ID of token owner.
  date: "date_example", # String | yyyy-MM-dd. Defaults to today.
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find projects applicable for time sheet registration on a specific day.
  result = api_instance.get_for_time_sheet(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->get_for_time_sheet: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employee_id** | **Integer**| Employee ID. Defaults to ID of token owner. | [optional] 
 **date** | **String**| yyyy-MM-dd. Defaults to today. | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseProject**](ListResponseProject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **post**
> ResponseWrapperProject post(opts)

[BETA] Add new project.



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

api_instance = TripletexApi::ProjectApi.new

opts = { 
  body: TripletexApi::Project.new # Project | JSON representing the new object to be created. Should not have ID and version set.
}

begin
  #[BETA] Add new project.
  result = api_instance.post(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Project**](Project.md)| JSON representing the new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ResponseWrapperProject**](ResponseWrapperProject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **post_list**
> ListResponseProject post_list(opts)

[BETA] Register new projects. Multiple projects for different users can be sent in the same request.



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

api_instance = TripletexApi::ProjectApi.new

opts = { 
  body: [TripletexApi::Project.new] # Array<Project> | JSON representing a list of new object to be created. Should not have ID and version set.
}

begin
  #[BETA] Register new projects. Multiple projects for different users can be sent in the same request.
  result = api_instance.post_list(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->post_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Array&lt;Project&gt;**](Project.md)| JSON representing a list of new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ListResponseProject**](ListResponseProject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put**
> ResponseWrapperProject put(id, opts)

[BETA] Update project.



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

api_instance = TripletexApi::ProjectApi.new

id = 56 # Integer | Element ID

opts = { 
  body: TripletexApi::Project.new # Project | Partial object describing what should be updated
}

begin
  #[BETA] Update project.
  result = api_instance.put(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **body** | [**Project**](Project.md)| Partial object describing what should be updated | [optional] 

### Return type

[**ResponseWrapperProject**](ResponseWrapperProject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put_list**
> ListResponseProject put_list(opts)

[BETA] Update multiple projects.



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

api_instance = TripletexApi::ProjectApi.new

opts = { 
  body: [TripletexApi::Project.new] # Array<Project> | JSON representing updates to object. Should have ID and version set.
}

begin
  #[BETA] Update multiple projects.
  result = api_instance.put_list(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->put_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Array&lt;Project&gt;**](Project.md)| JSON representing updates to object. Should have ID and version set. | [optional] 

### Return type

[**ListResponseProject**](ListResponseProject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **search**
> ListResponseProject search(opts)

Find projects corresponding with sent data.



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

api_instance = TripletexApi::ProjectApi.new

opts = { 
  id: "id_example", # String | List of IDs
  name: "name_example", # String | Containing
  number: "number_example", # String | Equals
  is_offer: true, # BOOLEAN | Equals
  project_manager_id: "project_manager_id_example", # String | List of IDs
  employee_in_project_id: "employee_in_project_id_example", # String | List of IDs
  department_id: "department_id_example", # String | List of IDs
  start_date_from: "start_date_from_example", # String | From and including
  start_date_to: "start_date_to_example", # String | To and excluding
  end_date_from: "end_date_from_example", # String | From and including
  end_date_to: "end_date_to_example", # String | To and excluding
  is_closed: true, # BOOLEAN | Equals
  customer_id: "customer_id_example", # String | Equals
  external_accounts_number: "external_accounts_number_example", # String | Containing
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find projects corresponding with sent data.
  result = api_instance.search(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling ProjectApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **String**| List of IDs | [optional] 
 **name** | **String**| Containing | [optional] 
 **number** | **String**| Equals | [optional] 
 **is_offer** | **BOOLEAN**| Equals | [optional] 
 **project_manager_id** | **String**| List of IDs | [optional] 
 **employee_in_project_id** | **String**| List of IDs | [optional] 
 **department_id** | **String**| List of IDs | [optional] 
 **start_date_from** | **String**| From and including | [optional] 
 **start_date_to** | **String**| To and excluding | [optional] 
 **end_date_from** | **String**| From and including | [optional] 
 **end_date_to** | **String**| To and excluding | [optional] 
 **is_closed** | **BOOLEAN**| Equals | [optional] 
 **customer_id** | **String**| Equals | [optional] 
 **external_accounts_number** | **String**| Containing | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ListResponseProject**](ListResponseProject.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



