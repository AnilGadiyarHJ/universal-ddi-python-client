# ScopeManagementResponse

The response format for scope management operations.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**ScopeManagementObject**](ScopeManagementObject.md) | Scope management configuration result | [optional] 

## Example

```python
from ipam_federation.models.scope_management_response import ScopeManagementResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ScopeManagementResponse from a JSON string
scope_management_response_instance = ScopeManagementResponse.from_json(json)
# print the JSON string representation of the object
print(ScopeManagementResponse.to_json())

# convert the object into a dict
scope_management_response_dict = scope_management_response_instance.to_dict()
# create an instance of ScopeManagementResponse from a dict
scope_management_response_from_dict = ScopeManagementResponse.from_dict(scope_management_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


