# ManageScopeTokenResponse

The response format containing the generated authentication token and metadata.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | JWT authentication token for the specified AWS IPAM scope | [optional] [readonly] 

## Example

```python
from ipam_federation.models.manage_scope_token_response import ManageScopeTokenResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ManageScopeTokenResponse from a JSON string
manage_scope_token_response_instance = ManageScopeTokenResponse.from_json(json)
# print the JSON string representation of the object
print(ManageScopeTokenResponse.to_json())

# convert the object into a dict
manage_scope_token_response_dict = manage_scope_token_response_instance.to_dict()
# create an instance of ManageScopeTokenResponse from a dict
manage_scope_token_response_from_dict = ManageScopeTokenResponse.from_dict(manage_scope_token_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


