# CreateForwardLookingDelegationResponse

The response format to create the __ForwardLookingDelegation__ object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**ForwardLookingDelegation**](ForwardLookingDelegation.md) | The created __ForwardLookingDelegation__ object. | [optional] 

## Example

```python
from ipam_federation.models.create_forward_looking_delegation_response import CreateForwardLookingDelegationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CreateForwardLookingDelegationResponse from a JSON string
create_forward_looking_delegation_response_instance = CreateForwardLookingDelegationResponse.from_json(json)
# print the JSON string representation of the object
print(CreateForwardLookingDelegationResponse.to_json())

# convert the object into a dict
create_forward_looking_delegation_response_dict = create_forward_looking_delegation_response_instance.to_dict()
# create an instance of CreateForwardLookingDelegationResponse from a dict
create_forward_looking_delegation_response_from_dict = CreateForwardLookingDelegationResponse.from_dict(create_forward_looking_delegation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


