# NextAvailableFLDRequest

A __ForwardLookingDelegation__ object (_federation/forward_looking_delegation_) is a set of contiguous IP addresses with no gap, expressed as a CIDR block. It may be used to allocate unique space for future resources which will ultimately hold a Delegation for the same CIDR block.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cidr** | **int** | The CIDR of the __ForwardLookingDelegation__. This is required. | 
**comment** | **str** | The description for the __ForwardLookingDelegation__. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
**count** | **int** | The count of __ForwardLookingDelegation__ required. If not provided, it will default to 1. | [optional] 
**name** | **str** | The name to be provided. | [optional] 
**protocol** | **str** | The version of the address (_ip4_ or _ip6_). If not present then it will default to _ip4_. | [optional] 
**tags** | **object** | The tags for the __ForwardLookingDelegation__ in JSON format. The tag will be used to identify the federated blocks which should be considered for __ForwardLookingDelegation__. | [optional] 

## Example

```python
from ipam_federation.models.next_available_fld_request import NextAvailableFLDRequest

# TODO update the JSON string below
json = "{}"
# create an instance of NextAvailableFLDRequest from a JSON string
next_available_fld_request_instance = NextAvailableFLDRequest.from_json(json)
# print the JSON string representation of the object
print(NextAvailableFLDRequest.to_json())

# convert the object into a dict
next_available_fld_request_dict = next_available_fld_request_instance.to_dict()
# create an instance of NextAvailableFLDRequest from a dict
next_available_fld_request_from_dict = NextAvailableFLDRequest.from_dict(next_available_fld_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


