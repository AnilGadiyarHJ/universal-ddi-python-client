# ListForwardLookingDelegationResponse

The response format to retrieve __ForwardLookingDelegation__ objects.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[ForwardLookingDelegation]**](ForwardLookingDelegation.md) | A list of __ForwardLookingDelegation__ objects. | [optional] 

## Example

```python
from ipam_federation.models.list_forward_looking_delegation_response import ListForwardLookingDelegationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListForwardLookingDelegationResponse from a JSON string
list_forward_looking_delegation_response_instance = ListForwardLookingDelegationResponse.from_json(json)
# print the JSON string representation of the object
print(ListForwardLookingDelegationResponse.to_json())

# convert the object into a dict
list_forward_looking_delegation_response_dict = list_forward_looking_delegation_response_instance.to_dict()
# create an instance of ListForwardLookingDelegationResponse from a dict
list_forward_looking_delegation_response_from_dict = ListForwardLookingDelegationResponse.from_dict(list_forward_looking_delegation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


