# ListFederatedPoolResponse

The response format to retrieve __FederatedPool__ objects.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | [**ApiPageInfo**](ApiPageInfo.md) | Page information including total_size when is_total_size_needed is requested. | [optional] 
**results** | [**List[FederatedPool]**](FederatedPool.md) | A list of FederatedPool objects. | [optional] 

## Example

```python
from ipam_federation.models.list_federated_pool_response import ListFederatedPoolResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListFederatedPoolResponse from a JSON string
list_federated_pool_response_instance = ListFederatedPoolResponse.from_json(json)
# print the JSON string representation of the object
print(ListFederatedPoolResponse.to_json())

# convert the object into a dict
list_federated_pool_response_dict = list_federated_pool_response_instance.to_dict()
# create an instance of ListFederatedPoolResponse from a dict
list_federated_pool_response_from_dict = ListFederatedPoolResponse.from_dict(list_federated_pool_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


