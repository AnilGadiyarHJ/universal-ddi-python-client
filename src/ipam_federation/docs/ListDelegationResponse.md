# ListDelegationResponse

The response format to retrieve __Delegation__ objects.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[Delegation]**](Delegation.md) | A list of Delegation objects. | [optional] 

## Example

```python
from ipam_federation.models.list_delegation_response import ListDelegationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListDelegationResponse from a JSON string
list_delegation_response_instance = ListDelegationResponse.from_json(json)
# print the JSON string representation of the object
print(ListDelegationResponse.to_json())

# convert the object into a dict
list_delegation_response_dict = list_delegation_response_instance.to_dict()
# create an instance of ListDelegationResponse from a dict
list_delegation_response_from_dict = ListDelegationResponse.from_dict(list_delegation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


