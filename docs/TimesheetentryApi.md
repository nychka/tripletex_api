# TripletexApi::TimesheetentryApi

All URIs are relative to *https://tripletex.no/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete**](TimesheetentryApi.md#delete) | **DELETE** /timesheet/entry/{id} | Delete timesheet entry by ID.
[**get**](TimesheetentryApi.md#get) | **GET** /timesheet/entry/{id} | Find timesheet entry by ID.
[**get_recent_activities**](TimesheetentryApi.md#get_recent_activities) | **GET** /timesheet/entry/&gt;recentActivities | Find recently used timesheet activities.
[**get_recent_projects**](TimesheetentryApi.md#get_recent_projects) | **GET** /timesheet/entry/&gt;recentProjects | Find projects with recent activities (timesheet entry registered).
[**get_total_hours**](TimesheetentryApi.md#get_total_hours) | **GET** /timesheet/entry/&gt;totalHours | Find total hours registered on an employee in a specific period.
[**post**](TimesheetentryApi.md#post) | **POST** /timesheet/entry | Add new timesheet entry. Only one entry per employee/date/activity/project combination is supported.
[**post_list**](TimesheetentryApi.md#post_list) | **POST** /timesheet/entry/list | Add new timesheet entry. Multiple objects for several users can be sent in the same request.
[**put**](TimesheetentryApi.md#put) | **PUT** /timesheet/entry/{id} | Update timesheet entry by ID. Note: Timesheet entry object fields which are present but not set, or set to 0, will be nulled.
[**put_list**](TimesheetentryApi.md#put_list) | **PUT** /timesheet/entry/list | Update timesheet entry. Multiple objects for different users can be sent in the same request.
[**search**](TimesheetentryApi.md#search) | **GET** /timesheet/entry | Find timesheet entry corresponding with sent data.


# **delete**
> delete(id, opts)

Delete timesheet entry by ID.



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

api_instance = TripletexApi::TimesheetentryApi.new

id = 56 # Integer | Element ID

opts = { 
  version: 56 # Integer | Number of current version
}

begin
  #Delete timesheet entry by ID.
  api_instance.delete(id, opts)
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->delete: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **version** | **Integer**| Number of current version | [optional] 

### Return type

nil (empty response body)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **get**
> ResponseWrapperTimesheetEntry get(id, opts)

Find timesheet entry by ID.



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

api_instance = TripletexApi::TimesheetentryApi.new

id = 56 # Integer | Element ID

opts = { 
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find timesheet entry by ID.
  result = api_instance.get(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->get: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperTimesheetEntry**](ResponseWrapperTimesheetEntry.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **get_recent_activities**
> ListResponseActivity get_recent_activities(project_id, opts)

Find recently used timesheet activities.



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

api_instance = TripletexApi::TimesheetentryApi.new

project_id = 56 # Integer | ID of project to find activities for

opts = { 
  employee_id: 56, # Integer | ID of employee to find activities for. Defaults to ID of token owner.
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find recently used timesheet activities.
  result = api_instance.get_recent_activities(project_id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->get_recent_activities: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **Integer**| ID of project to find activities for | 
 **employee_id** | **Integer**| ID of employee to find activities for. Defaults to ID of token owner. | [optional] 
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



# **get_recent_projects**
> ListResponseProject get_recent_projects(opts)

Find projects with recent activities (timesheet entry registered).



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

api_instance = TripletexApi::TimesheetentryApi.new

opts = { 
  employee_id: 56, # Integer | ID of employee with recent project hours Defaults to ID of token owner.
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find projects with recent activities (timesheet entry registered).
  result = api_instance.get_recent_projects(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->get_recent_projects: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employee_id** | **Integer**| ID of employee with recent project hours Defaults to ID of token owner. | [optional] 
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



# **get_total_hours**
> ResponseWrapperDouble get_total_hours(opts)

Find total hours registered on an employee in a specific period.



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

api_instance = TripletexApi::TimesheetentryApi.new

opts = { 
  employee_id: 56, # Integer | ID of employee to find hours for. Defaults to ID of token owner.
  start_date: "start_date_example", # String | Format is yyyy-MM-dd (from and incl.). Defaults to today.
  end_date: "end_date_example", # String | Format is yyyy-MM-dd (to and excl.). Defaults to tomorrow.
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find total hours registered on an employee in a specific period.
  result = api_instance.get_total_hours(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->get_total_hours: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **employee_id** | **Integer**| ID of employee to find hours for. Defaults to ID of token owner. | [optional] 
 **start_date** | **String**| Format is yyyy-MM-dd (from and incl.). Defaults to today. | [optional] 
 **end_date** | **String**| Format is yyyy-MM-dd (to and excl.). Defaults to tomorrow. | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**ResponseWrapperDouble**](ResponseWrapperDouble.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



# **post**
> ResponseWrapperTimesheetEntry post(opts)

Add new timesheet entry. Only one entry per employee/date/activity/project combination is supported.



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

api_instance = TripletexApi::TimesheetentryApi.new

opts = { 
  body: TripletexApi::TimesheetEntry.new # TimesheetEntry | JSON representing the new object to be created. Should not have ID and version set.
}

begin
  #Add new timesheet entry. Only one entry per employee/date/activity/project combination is supported.
  result = api_instance.post(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**TimesheetEntry**](TimesheetEntry.md)| JSON representing the new object to be created. Should not have ID and version set. | [optional] 

### Return type

[**ResponseWrapperTimesheetEntry**](ResponseWrapperTimesheetEntry.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **post_list**
> ListResponseTimesheetEntry post_list(opts)

Add new timesheet entry. Multiple objects for several users can be sent in the same request.



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

api_instance = TripletexApi::TimesheetentryApi.new

opts = { 
  body: [TripletexApi::TimesheetEntry.new] # Array<TimesheetEntry> | List of timesheet entry objects
}

begin
  #Add new timesheet entry. Multiple objects for several users can be sent in the same request.
  result = api_instance.post_list(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->post_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Array&lt;TimesheetEntry&gt;**](TimesheetEntry.md)| List of timesheet entry objects | [optional] 

### Return type

[**ListResponseTimesheetEntry**](ListResponseTimesheetEntry.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put**
> ResponseWrapperTimesheetEntry put(id, opts)

Update timesheet entry by ID. Note: Timesheet entry object fields which are present but not set, or set to 0, will be nulled.



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

api_instance = TripletexApi::TimesheetentryApi.new

id = 56 # Integer | Element ID

opts = { 
  body: TripletexApi::TimesheetEntry.new # TimesheetEntry | Partial object describing what should be updated
}

begin
  #Update timesheet entry by ID. Note: Timesheet entry object fields which are present but not set, or set to 0, will be nulled.
  result = api_instance.put(id, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->put: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **Integer**| Element ID | 
 **body** | [**TimesheetEntry**](TimesheetEntry.md)| Partial object describing what should be updated | [optional] 

### Return type

[**ResponseWrapperTimesheetEntry**](ResponseWrapperTimesheetEntry.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **put_list**
> ListResponseTimesheetEntry put_list(opts)

Update timesheet entry. Multiple objects for different users can be sent in the same request.



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

api_instance = TripletexApi::TimesheetentryApi.new

opts = { 
  body: [TripletexApi::TimesheetEntry.new] # Array<TimesheetEntry> | List of timesheet entry objects to update
}

begin
  #Update timesheet entry. Multiple objects for different users can be sent in the same request.
  result = api_instance.put_list(opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->put_list: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Array&lt;TimesheetEntry&gt;**](TimesheetEntry.md)| List of timesheet entry objects to update | [optional] 

### Return type

[**ListResponseTimesheetEntry**](ListResponseTimesheetEntry.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: application/json; charset=utf-8
 - **Accept**: Not defined



# **search**
> TimesheetEntrySearchResponse search(date_from, date_to, opts)

Find timesheet entry corresponding with sent data.



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

api_instance = TripletexApi::TimesheetentryApi.new

date_from = "date_from_example" # String | From and including

date_to = "date_to_example" # String | To and excluding

opts = { 
  id: "id_example", # String | List of IDs
  employee_id: "employee_id_example", # String | List of IDs
  project_id: "project_id_example", # String | List of IDs
  activity_id: "activity_id_example", # String | List of IDs
  comment: "comment_example", # String | Containing
  from: 0, # Integer | From index
  count: 1000, # Integer | Number of elements to return
  sorting: "sorting_example", # String | Sorting pattern
  fields: "fields_example" # String | Fields filter pattern
}

begin
  #Find timesheet entry corresponding with sent data.
  result = api_instance.search(date_from, date_to, opts)
  p result
rescue TripletexApi::ApiError => e
  puts "Exception when calling TimesheetentryApi->search: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **date_from** | **String**| From and including | 
 **date_to** | **String**| To and excluding | 
 **id** | **String**| List of IDs | [optional] 
 **employee_id** | **String**| List of IDs | [optional] 
 **project_id** | **String**| List of IDs | [optional] 
 **activity_id** | **String**| List of IDs | [optional] 
 **comment** | **String**| Containing | [optional] 
 **from** | **Integer**| From index | [optional] [default to 0]
 **count** | **Integer**| Number of elements to return | [optional] [default to 1000]
 **sorting** | **String**| Sorting pattern | [optional] 
 **fields** | **String**| Fields filter pattern | [optional] 

### Return type

[**TimesheetEntrySearchResponse**](TimesheetEntrySearchResponse.md)

### Authorization

[tokenAuthScheme](../README.md#tokenAuthScheme)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined



