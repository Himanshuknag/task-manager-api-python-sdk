# CreateTaskRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** | Short title of the task | 
**description** | **str** | Longer description of the task | [optional] 
**assignee** | **str** | Email of the person assigned to the task | [optional] 
**priority** | **str** | Priority level of the task | [optional] 
**due_date** | **date** | Due date for the task (YYYY-MM-DD) | [optional] 

## Example

```python
from probestack_sdk.models.create_task_request import CreateTaskRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateTaskRequest from a JSON string
create_task_request_instance = CreateTaskRequest.from_json(json)
# print the JSON string representation of the object
print(CreateTaskRequest.to_json())

# convert the object into a dict
create_task_request_dict = create_task_request_instance.to_dict()
# create an instance of CreateTaskRequest from a dict
create_task_request_from_dict = CreateTaskRequest.from_dict(create_task_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


