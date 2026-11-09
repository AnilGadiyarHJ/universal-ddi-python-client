# Delegation

A __Delegation__ object (_federation/delegation_) is a set of contiguous IP addresses with no gap, expressed as a CIDR block. A Delegation is explicitly associated with Federated Realms, and implicitly with Federated Block Parents. A Delegation in a given realm is said to be the child of the closest enclosing parent.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **str** | The address field in form “a.b.c.d/n” where the “/n” may be omitted. In this case, the CIDR value must be defined in the _cidr_ field. When reading, the _address_ field is always in the form “a.b.c.d”. | 
**cidr** | **int** | The CIDR of the delegation. This is required, if _address_ does not specify it in its input. | [optional] 
**comment** | **str** | The description for the delegation. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
**created_at** | **datetime** | Time when the object has been created. | [optional] [readonly] 
**delegated_to** | **str** | The specific IPAM service the delegation was delegated to. In case federated realms are not provided, this field would be used to determine the __Federated_Realm__ the __Delegation__ should be part of. | 
**federated_pool_id** | **str** | The resource identifier. | [optional] 
**federated_realms** | **List[str]** | The resource identifier. | [optional] 
**id** | **str** | The resource identifier. | [optional] [readonly] 
**metadata** | **object** | The metadata for the delegation in JSON format. | [optional] 
**name** | **str** | The name of the delegation. May contain 1 to 256 characters. Can include UTF-8. | [optional] 
**parents** | **List[str]** | The resource identifier. | [optional] 
**protocol** | **str** | The type of protocol of delegation (_ip4_ or _ip6_). | [optional] [readonly] 
**region** | **str** | The region where the delegation is located. | [optional] 
**tags** | **object** | The tags for the delegation in JSON format. | [optional] 
**updated_at** | **datetime** | Time when the object has been updated. Equals to _created_at_ if not updated after creation. | [optional] [readonly] 
**utilization** | **int** | The IP address utilization percentage of the object _federation/delegation_. | [optional] [readonly] 

## Example

```python
from ipam_federation.models.delegation import Delegation

# TODO update the JSON string below
json = "{}"
# create an instance of Delegation from a JSON string
delegation_instance = Delegation.from_json(json)
# print the JSON string representation of the object
print(Delegation.to_json())

# convert the object into a dict
delegation_dict = delegation_instance.to_dict()
# create an instance of Delegation from a dict
delegation_from_dict = Delegation.from_dict(delegation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


