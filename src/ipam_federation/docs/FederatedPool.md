# FederatedPool

A __FederatedPool__ object (_federation/federated_pool_) represents a group of federated blocks that can be allocated for specific providers and regions. Federated pools are hierarchical and may be parented to other federated pools. Top level federated pools are parented to a federated realm.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allocation** | [**Allocation**](Allocation.md) | The allocation details for the __FederatedPool__. | [optional] [readonly] 
**created_at** | **datetime** | Time when the object has been created. | [optional] [readonly] 
**description** | **str** | The description for the federated pool. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
**federated_realm** | **str** | The resource identifier. | 
**id** | **str** | The resource identifier. | [optional] [readonly] 
**metadata** | **object** | The metadata for the federated pool in JSON format. | [optional] 
**name** | **str** | The name of the federated pool. May contain 1 to 256 characters. Can include UTF-8. | [optional] 
**network_compliance** | [**NetworkCompliance**](NetworkCompliance.md) | The network compliance of the __FederatedPool__. | [optional] 
**network_compliant** | **bool** | Indicates if this pool is compliant with its parent&#39;s network compliance policy. When false, a trouble dot should be displayed in the UI to indicate non-compliance. | [optional] [readonly] 
**parent** | **str** | The resource identifier. | [optional] 
**protocol** | **str** | The address family of the pool (&#39;ip4&#39;, &#39;ip6&#39;, or &#39;ip4/ip6&#39; for dual mode support on NIOS_X pools only). | 
**provider** | [**ProviderType**](ProviderType.md) | The cloud provider type this pool is associated with. | 
**region** | **str** | The region/locale this pool is associated with (e.g., &#39;us-west-1&#39;, &#39;eu-central-1&#39;). | 
**state** | **str** | The current state of the federated pool (e.g., &#39;create-complete&#39;, &#39;create-in-progress&#39;, &#39;delete-in-progress&#39;). | [optional] [readonly] 
**tags** | **object** | The tags for the federated pool in JSON format. | [optional] 
**updated_at** | **datetime** | Time when the object has been updated. Equals to _created_at_ if not updated after creation. | [optional] [readonly] 
**utilization** | **int** | The IPv4 utilization percentage of the __FederatedPool__. | [optional] [readonly] 
**utilization_v6** | [**UtilizationV6**](UtilizationV6.md) | The IPv6 utilization metrics for the __FederatedPool__. | [optional] [readonly] 

## Example

```python
from ipam_federation.models.federated_pool import FederatedPool

# TODO update the JSON string below
json = "{}"
# create an instance of FederatedPool from a JSON string
federated_pool_instance = FederatedPool.from_json(json)
# print the JSON string representation of the object
print(FederatedPool.to_json())

# convert the object into a dict
federated_pool_dict = federated_pool_instance.to_dict()
# create an instance of FederatedPool from a dict
federated_pool_from_dict = FederatedPool.from_dict(federated_pool_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


