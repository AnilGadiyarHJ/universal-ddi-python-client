# UpdateFederatedPoolResponse

The response format to update the __FederatedPool__ object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**FederatedPool**](FederatedPool.md) | The FederatedPool object. | [optional] 

## Example

```python
from ipam_federation.models.update_federated_pool_response import UpdateFederatedPoolResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateFederatedPoolResponse from a JSON string
update_federated_pool_response_instance = UpdateFederatedPoolResponse.from_json(json)
# print the JSON string representation of the object
print(UpdateFederatedPoolResponse.to_json())

# convert the object into a dict
update_federated_pool_response_dict = update_federated_pool_response_instance.to_dict()
# create an instance of UpdateFederatedPoolResponse from a dict
update_federated_pool_response_from_dict = UpdateFederatedPoolResponse.from_dict(update_federated_pool_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


