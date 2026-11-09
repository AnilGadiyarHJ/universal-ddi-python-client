# ManageScopeTokenRequest

The request format to generate an authentication token for AWS IPAM scope.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** | The Infoblox account ID for which the token is generated. | 
**scope_arn** | **str** |  | 
**ttl** | **int** | Optional token expiration duration in seconds. Defaults to 300 (5 minutes) if not specified or set to 0. Maximum allowed: 86400 (24 hours), Minimum: 0 (uses default). | [optional] 

## Example

```python
from ipam_federation.models.manage_scope_token_request import ManageScopeTokenRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ManageScopeTokenRequest from a JSON string
manage_scope_token_request_instance = ManageScopeTokenRequest.from_json(json)
# print the JSON string representation of the object
print(ManageScopeTokenRequest.to_json())

# convert the object into a dict
manage_scope_token_request_dict = manage_scope_token_request_instance.to_dict()
# create an instance of ManageScopeTokenRequest from a dict
manage_scope_token_request_from_dict = ManageScopeTokenRequest.from_dict(manage_scope_token_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


