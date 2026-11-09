# NetworkCompliance

The __NetworkCompliance__ represents the network compliance of federated pool and federated block.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**default_netmask_length** | **int** | The default netmask length used when allocating child blocks or pools. | [optional] 
**maximum_netmask_length** | **int** | The maximum netmask length for allocating child blocks or pools. | [optional] 
**minimum_netmask_length** | **int** | The minimum netmask length for allocating child blocks or pools. | [optional] 

## Example

```python
from ipam_federation.models.network_compliance import NetworkCompliance

# TODO update the JSON string below
json = "{}"
# create an instance of NetworkCompliance from a JSON string
network_compliance_instance = NetworkCompliance.from_json(json)
# print the JSON string representation of the object
print(NetworkCompliance.to_json())

# convert the object into a dict
network_compliance_dict = network_compliance_instance.to_dict()
# create an instance of NetworkCompliance from a dict
network_compliance_from_dict = NetworkCompliance.from_dict(network_compliance_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


