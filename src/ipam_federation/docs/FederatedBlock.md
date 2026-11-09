# FederatedBlock

A __FederatedBlock__ object (_federation/federated_block_) is a set of contiguous IP addresses with no gap, expressed as a CIDR block. Federated blocks are hierarchical and may be parented to other federated blocks as long as the parent block fully contains the child and no sibling overlaps. Top level federated blocks are parented to a federated realm.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **str** | The address field in form “a.b.c.d/n” where the “/n” may be omitted. In this case, the CIDR value must be defined in the _cidr_ field. When reading, the _address_ field is always in the form “a.b.c.d”. | 
**allocation_v4** | [**Allocation**](Allocation.md) | The percentage of the Federated Block’s total address space that is consumed by Leaf Terminals. | [optional] 
**cidr** | **int** | The CIDR of the federated block. This is required, if _address_ does not specify it in its input. | [optional] 
**comment** | **str** | The description for the federated block. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
**created_at** | **datetime** | Time when the object has been created. | [optional] [readonly] 
**federated_pool_id** | **str** | The resource identifier. | [optional] 
**federated_realm** | **str** | The resource identifier. | 
**id** | **str** | The resource identifier. | [optional] [readonly] 
**metadata** | **object** | The metadata for the federated block in JSON format. | [optional] 
**name** | **str** | The name of the federated block. May contain 1 to 256 characters. Can include UTF-8. | [optional] 
**network_compliance** | [**NetworkCompliance**](NetworkCompliance.md) | The network compliance policy for child objects. This defines the minimum, default, and maximum netmask lengths that can be used when creating child blocks. | [optional] 
**network_compliant** | **bool** | Indicates if this block is compliant with its parent&#39;s network compliance policy. When false, a trouble dot should be displayed in the UI to indicate non-compliance. | [optional] [readonly] 
**parent** | **str** | The resource identifier. | [optional] 
**protocol** | **str** | The type of protocol of federated block (_ip4_ or _ip6_). | [optional] [readonly] 
**region** | **str** | The region where the federated block is located. | [optional] 
**state** | **str** |  | [optional] 
**tags** | **object** | The tags for the federated block in JSON format. | [optional] 
**updated_at** | **datetime** | Time when the object has been updated. Equals to _created_at_ if not updated after creation. | [optional] [readonly] 
**utilization** | **int** | The percentage of Federated Block utilization. | [optional] 
**utilization_v6** | [**UtilizationV6**](UtilizationV6.md) | The IPv6 utilization metrics for the federated block. | [optional] [readonly] 

## Example

```python
from ipam_federation.models.federated_block import FederatedBlock

# TODO update the JSON string below
json = "{}"
# create an instance of FederatedBlock from a JSON string
federated_block_instance = FederatedBlock.from_json(json)
# print the JSON string representation of the object
print(FederatedBlock.to_json())

# convert the object into a dict
federated_block_dict = federated_block_instance.to_dict()
# create an instance of FederatedBlock from a dict
federated_block_from_dict = FederatedBlock.from_dict(federated_block_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


