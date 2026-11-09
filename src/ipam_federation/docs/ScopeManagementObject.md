# ScopeManagementObject

The scope management configuration details.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enable** | **bool** | Whether to enable (true) or disable (false) scope management. Defaults to false if not specified. | [optional] 
**scope_arn** | **str** | AWS IPAM scope ARN to be set as externally managed | 

## Example

```python
from ipam_federation.models.scope_management_object import ScopeManagementObject

# TODO update the JSON string below
json = "{}"
# create an instance of ScopeManagementObject from a JSON string
scope_management_object_instance = ScopeManagementObject.from_json(json)
# print the JSON string representation of the object
print(ScopeManagementObject.to_json())

# convert the object into a dict
scope_management_object_dict = scope_management_object_instance.to_dict()
# create an instance of ScopeManagementObject from a dict
scope_management_object_from_dict = ScopeManagementObject.from_dict(scope_management_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


