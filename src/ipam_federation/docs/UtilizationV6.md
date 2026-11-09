# UtilizationV6

The __UtilizationV6__ represents IPv6 utilization metrics.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **bytearray** |  | [optional] 
**used** | **bytearray** |  | [optional] 

## Example

```python
from ipam_federation.models.utilization_v6 import UtilizationV6

# TODO update the JSON string below
json = "{}"
# create an instance of UtilizationV6 from a JSON string
utilization_v6_instance = UtilizationV6.from_json(json)
# print the JSON string representation of the object
print(UtilizationV6.to_json())

# convert the object into a dict
utilization_v6_dict = utilization_v6_instance.to_dict()
# create an instance of UtilizationV6 from a dict
utilization_v6_from_dict = UtilizationV6.from_dict(utilization_v6_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


