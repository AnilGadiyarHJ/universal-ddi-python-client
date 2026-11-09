# UpdateForwardLookingDelegationResponse

The response format to update the __ForwardLookingDelegation__ object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**ForwardLookingDelegation**](ForwardLookingDelegation.md) | The updated __ForwardLookingDelegation__ object. | [optional] 

## Example

```python
from ipam_federation.models.update_forward_looking_delegation_response import UpdateForwardLookingDelegationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateForwardLookingDelegationResponse from a JSON string
update_forward_looking_delegation_response_instance = UpdateForwardLookingDelegationResponse.from_json(json)
# print the JSON string representation of the object
print(UpdateForwardLookingDelegationResponse.to_json())

# convert the object into a dict
update_forward_looking_delegation_response_dict = update_forward_looking_delegation_response_instance.to_dict()
# create an instance of UpdateForwardLookingDelegationResponse from a dict
update_forward_looking_delegation_response_from_dict = UpdateForwardLookingDelegationResponse.from_dict(update_forward_looking_delegation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


