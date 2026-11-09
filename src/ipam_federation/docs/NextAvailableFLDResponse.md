# NextAvailableFLDResponse

The response format to list next available __ForwardLookingDelegation__ objects.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[ForwardLookingDelegation]**](ForwardLookingDelegation.md) |  | [optional] 

## Example

```python
from ipam_federation.models.next_available_fld_response import NextAvailableFLDResponse

# TODO update the JSON string below
json = "{}"
# create an instance of NextAvailableFLDResponse from a JSON string
next_available_fld_response_instance = NextAvailableFLDResponse.from_json(json)
# print the JSON string representation of the object
print(NextAvailableFLDResponse.to_json())

# convert the object into a dict
next_available_fld_response_dict = next_available_fld_response_instance.to_dict()
# create an instance of NextAvailableFLDResponse from a dict
next_available_fld_response_from_dict = NextAvailableFLDResponse.from_dict(next_available_fld_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


