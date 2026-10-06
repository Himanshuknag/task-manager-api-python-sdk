# UpdateTaskRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** | Updated title | [optional] 
**status** | **str** | New status for the task | 
**priority** | **str** |  | [optional] 
**completed** | **bool** | Whether the task is fully completed | [optional] 

## Example

```python
from probestack_sdk.models.update_task_request import UpdateTaskRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateTaskRequest from a JSON string
update_task_request_instance = UpdateTaskRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateTaskRequest.to_json())

# convert the object into a dict
update_task_request_dict = update_task_request_instance.to_dict()
# create an instance of UpdateTaskRequest from a dict
update_task_request_from_dict = UpdateTaskRequest.from_dict(update_task_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


