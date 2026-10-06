# AddTaskCommentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Comment text | 
**author** | **str** | Email of the comment author | 
**tags** | **List[str]** | Optional tags attached to the comment | [optional] 

## Example

```python
from probestack_sdk.models.add_task_comment_request import AddTaskCommentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddTaskCommentRequest from a JSON string
add_task_comment_request_instance = AddTaskCommentRequest.from_json(json)
# print the JSON string representation of the object
print(AddTaskCommentRequest.to_json())

# convert the object into a dict
add_task_comment_request_dict = add_task_comment_request_instance.to_dict()
# create an instance of AddTaskCommentRequest from a dict
add_task_comment_request_from_dict = AddTaskCommentRequest.from_dict(add_task_comment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


