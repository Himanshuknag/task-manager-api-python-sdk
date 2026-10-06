# probestack_sdk.DefaultApi

All URIs are relative to *https://api.taskmanager.example.com/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_task_comment**](DefaultApi.md#add_task_comment) | **POST** /tasks/{taskId}/comments | Add a comment to a task
[**create_task**](DefaultApi.md#create_task) | **POST** /tasks | Create a new task
[**delete_task**](DefaultApi.md#delete_task) | **DELETE** /tasks/{taskId} | Delete a task
[**get_task_by_id**](DefaultApi.md#get_task_by_id) | **GET** /tasks/{taskId} | Get a task by ID
[**list_tasks**](DefaultApi.md#list_tasks) | **GET** /tasks | List all tasks
[**update_task**](DefaultApi.md#update_task) | **PUT** /tasks/{taskId} | Update an existing task


# **add_task_comment**
> add_task_comment(task_id, add_task_comment_request)

Add a comment to a task

Adds a new comment with optional tags to the specified task's activity log.

### Example


```python
import probestack_sdk
from probestack_sdk.models.add_task_comment_request import AddTaskCommentRequest
from probestack_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.taskmanager.example.com/v3
# See configuration.py for a list of all supported configuration parameters.
configuration = probestack_sdk.Configuration(
    host = "https://api.taskmanager.example.com/v3"
)


# Enter a context with an instance of the API client
with probestack_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = probestack_sdk.DefaultApi(api_client)
    task_id = 'task_id_example' # str | Unique ID of the task
    add_task_comment_request = probestack_sdk.AddTaskCommentRequest() # AddTaskCommentRequest | 

    try:
        # Add a comment to a task
        api_instance.add_task_comment(task_id, add_task_comment_request)
    except Exception as e:
        print("Exception when calling DefaultApi->add_task_comment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | **str**| Unique ID of the task | 
 **add_task_comment_request** | [**AddTaskCommentRequest**](AddTaskCommentRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Comment added |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_task**
> Task create_task(create_task_request)

Create a new task

Creates a new task with a title and optional description, assignee, priority and due date.

### Example


```python
import probestack_sdk
from probestack_sdk.models.create_task_request import CreateTaskRequest
from probestack_sdk.models.task import Task
from probestack_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.taskmanager.example.com/v3
# See configuration.py for a list of all supported configuration parameters.
configuration = probestack_sdk.Configuration(
    host = "https://api.taskmanager.example.com/v3"
)


# Enter a context with an instance of the API client
with probestack_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = probestack_sdk.DefaultApi(api_client)
    create_task_request = probestack_sdk.CreateTaskRequest() # CreateTaskRequest | 

    try:
        # Create a new task
        api_response = api_instance.create_task(create_task_request)
        print("The response of DefaultApi->create_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->create_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_task_request** | [**CreateTaskRequest**](CreateTaskRequest.md)|  | 

### Return type

[**Task**](Task.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Task created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_task**
> delete_task(task_id)

Delete a task

Permanently deletes a task by ID.

### Example


```python
import probestack_sdk
from probestack_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.taskmanager.example.com/v3
# See configuration.py for a list of all supported configuration parameters.
configuration = probestack_sdk.Configuration(
    host = "https://api.taskmanager.example.com/v3"
)


# Enter a context with an instance of the API client
with probestack_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = probestack_sdk.DefaultApi(api_client)
    task_id = 'task_id_example' # str | Unique ID of the task to delete

    try:
        # Delete a task
        api_instance.delete_task(task_id)
    except Exception as e:
        print("Exception when calling DefaultApi->delete_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | **str**| Unique ID of the task to delete | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Task deleted successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task_by_id**
> Task get_task_by_id(task_id)

Get a task by ID

Retrieves a single task by its unique identifier.

### Example


```python
import probestack_sdk
from probestack_sdk.models.task import Task
from probestack_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.taskmanager.example.com/v3
# See configuration.py for a list of all supported configuration parameters.
configuration = probestack_sdk.Configuration(
    host = "https://api.taskmanager.example.com/v3"
)


# Enter a context with an instance of the API client
with probestack_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = probestack_sdk.DefaultApi(api_client)
    task_id = 'task_id_example' # str | Unique ID of the task

    try:
        # Get a task by ID
        api_response = api_instance.get_task_by_id(task_id)
        print("The response of DefaultApi->get_task_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->get_task_by_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | **str**| Unique ID of the task | 

### Return type

[**Task**](Task.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Task found |  -  |
**404** | Task not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_tasks**
> List[Task] list_tasks(status=status, limit=limit)

List all tasks

Returns tasks, optionally filtered by status, with an optional page-size limit.

### Example


```python
import probestack_sdk
from probestack_sdk.models.task import Task
from probestack_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.taskmanager.example.com/v3
# See configuration.py for a list of all supported configuration parameters.
configuration = probestack_sdk.Configuration(
    host = "https://api.taskmanager.example.com/v3"
)


# Enter a context with an instance of the API client
with probestack_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = probestack_sdk.DefaultApi(api_client)
    status = 'status_example' # str | Filter tasks by status (optional)
    limit = 20 # int | Maximum number of tasks to return (optional) (default to 20)

    try:
        # List all tasks
        api_response = api_instance.list_tasks(status=status, limit=limit)
        print("The response of DefaultApi->list_tasks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->list_tasks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **status** | **str**| Filter tasks by status | [optional] 
 **limit** | **int**| Maximum number of tasks to return | [optional] [default to 20]

### Return type

[**List[Task]**](Task.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A list of tasks |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_task**
> Task update_task(task_id, update_task_request)

Update an existing task

Updates fields of an existing task, including its status and completion flag.

### Example


```python
import probestack_sdk
from probestack_sdk.models.task import Task
from probestack_sdk.models.update_task_request import UpdateTaskRequest
from probestack_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.taskmanager.example.com/v3
# See configuration.py for a list of all supported configuration parameters.
configuration = probestack_sdk.Configuration(
    host = "https://api.taskmanager.example.com/v3"
)


# Enter a context with an instance of the API client
with probestack_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = probestack_sdk.DefaultApi(api_client)
    task_id = 'task_id_example' # str | Unique ID of the task to update
    update_task_request = probestack_sdk.UpdateTaskRequest() # UpdateTaskRequest | 

    try:
        # Update an existing task
        api_response = api_instance.update_task(task_id, update_task_request)
        print("The response of DefaultApi->update_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DefaultApi->update_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **task_id** | **str**| Unique ID of the task to update | 
 **update_task_request** | [**UpdateTaskRequest**](UpdateTaskRequest.md)|  | 

### Return type

[**Task**](Task.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Task updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

