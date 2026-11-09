# CreateFederatedPoolResponse

The response format to create the __FederatedPool__ object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**FederatedPool**](FederatedPool.md) | The created FederatedPool object. | [optional] 

## Example

```python
from ipam_federation.models.create_federated_pool_response import CreateFederatedPoolResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CreateFederatedPoolResponse from a JSON string
create_federated_pool_response_instance = CreateFederatedPoolResponse.from_json(json)
# print the JSON string representation of the object
print(CreateFederatedPoolResponse.to_json())

# convert the object into a dict
create_federated_pool_response_dict = create_federated_pool_response_instance.to_dict()
# create an instance of CreateFederatedPoolResponse from a dict
create_federated_pool_response_from_dict = CreateFederatedPoolResponse.from_dict(create_federated_pool_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


