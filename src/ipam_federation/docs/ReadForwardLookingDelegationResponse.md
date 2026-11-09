# ReadForwardLookingDelegationResponse

The response format to retrieve the __ForwardLookingDelegation__ object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**ForwardLookingDelegation**](ForwardLookingDelegation.md) | The __ForwardLookingDelegation__ object. | [optional] 

## Example

```python
from ipam_federation.models.read_forward_looking_delegation_response import ReadForwardLookingDelegationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReadForwardLookingDelegationResponse from a JSON string
read_forward_looking_delegation_response_instance = ReadForwardLookingDelegationResponse.from_json(json)
# print the JSON string representation of the object
print(ReadForwardLookingDelegationResponse.to_json())

# convert the object into a dict
read_forward_looking_delegation_response_dict = read_forward_looking_delegation_response_instance.to_dict()
# create an instance of ReadForwardLookingDelegationResponse from a dict
read_forward_looking_delegation_response_from_dict = ReadForwardLookingDelegationResponse.from_dict(read_forward_looking_delegation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


