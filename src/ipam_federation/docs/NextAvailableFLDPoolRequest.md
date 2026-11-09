# NextAvailableFLDPoolRequest

Request to list or allocate the next available __ForwardLookingDelegation__ objects within a specific _federated_pool_.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cidr** | **int** | The CIDR prefix length of the __ForwardLookingDelegation__ to allocate. Required. | 
**comment** | **str** | The description for the allocated __ForwardLookingDelegation__ objects. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
**count** | **int** | The number of __ForwardLookingDelegation__ objects to allocate. Defaults to 1 if not provided. Maximum is 20. | [optional] 
**id** | **str** | The resource identifier. | [readonly] 
**name** | **str** | The name to assign to the allocated __ForwardLookingDelegation__ objects. | [optional] 
**protocol** | **str** | The IP version of the __ForwardLookingDelegation__ (_ip4_ or _ip6_). Defaults to _ip4_ if not provided. | [optional] 
**tags** | **object** | The tags for the allocated __ForwardLookingDelegation__ objects in JSON format. | [optional] 

## Example

```python
from ipam_federation.models.next_available_fld_pool_request import NextAvailableFLDPoolRequest

# TODO update the JSON string below
json = "{}"
# create an instance of NextAvailableFLDPoolRequest from a JSON string
next_available_fld_pool_request_instance = NextAvailableFLDPoolRequest.from_json(json)
# print the JSON string representation of the object
print(NextAvailableFLDPoolRequest.to_json())

# convert the object into a dict
next_available_fld_pool_request_dict = next_available_fld_pool_request_instance.to_dict()
# create an instance of NextAvailableFLDPoolRequest from a dict
next_available_fld_pool_request_from_dict = NextAvailableFLDPoolRequest.from_dict(next_available_fld_pool_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


