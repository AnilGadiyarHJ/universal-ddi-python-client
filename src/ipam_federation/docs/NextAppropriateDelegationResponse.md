# NextAppropriateDelegationResponse

The response format to retrieve __Delegation__ objects.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[Delegation]**](Delegation.md) | A list of __Delegation__ objects. | [optional] 

## Example

```python
from ipam_federation.models.next_appropriate_delegation_response import NextAppropriateDelegationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of NextAppropriateDelegationResponse from a JSON string
next_appropriate_delegation_response_instance = NextAppropriateDelegationResponse.from_json(json)
# print the JSON string representation of the object
print(NextAppropriateDelegationResponse.to_json())

# convert the object into a dict
next_appropriate_delegation_response_dict = next_appropriate_delegation_response_instance.to_dict()
# create an instance of NextAppropriateDelegationResponse from a dict
next_appropriate_delegation_response_from_dict = NextAppropriateDelegationResponse.from_dict(next_appropriate_delegation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


