# ReadFederatedPoolResponse

The response format to retrieve the __FederatedPool__ object.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**result** | [**FederatedPool**](FederatedPool.md) | The FederatedPool object. | [optional] 

## Example

```python
from ipam_federation.models.read_federated_pool_response import ReadFederatedPoolResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReadFederatedPoolResponse from a JSON string
read_federated_pool_response_instance = ReadFederatedPoolResponse.from_json(json)
# print the JSON string representation of the object
print(ReadFederatedPoolResponse.to_json())

# convert the object into a dict
read_federated_pool_response_dict = read_federated_pool_response_instance.to_dict()
# create an instance of ReadFederatedPoolResponse from a dict
read_federated_pool_response_from_dict = ReadFederatedPoolResponse.from_dict(read_federated_pool_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


