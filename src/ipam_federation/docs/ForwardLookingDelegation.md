# ForwardLookingDelegation

A __ForwardLookingDelegation__ object (_federation/forward_looking_delegation_) is a set of contiguous IP addresses with no gap, expressed as a CIDR block. It may be used to allocate unique space for future resources which will ultimately hold a Delegation for the same CIDR block.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **str** | The address field in form “a.b.c.d/n” where the “/n” may be omitted. In this case, the CIDR value must be defined in the _cidr_ field. When reading, the _address_ field is always in the form “a.b.c.d”. | 
**cidr** | **int** | The CIDR of the delegation. This is required, if _address_ does not specify it in its input. | [optional] 
**comment** | **str** | The description for the delegation. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
**created_at** | **datetime** | Time when the object has been created. | [optional] [readonly] 
**federated_pool_id** | **str** | The resource identifier. | [optional] 
**federated_realms** | **List[str]** | The resource identifier. | 
**id** | **str** | The resource identifier. | [optional] [readonly] 
**name** | **str** | The name of the delegation. May contain 1 to 256 characters. Can include UTF-8. | [optional] 
**network_compliant** | **bool** | The compliance status of the forward looking delegation, as determined by the federation service. | [optional] [readonly] 
**protocol** | **str** | The type of protocol of delegation (_ip4_ or _ip6_). | [optional] [readonly] 
**tags** | **object** | The tags for the delegation in JSON format. | [optional] 
**updated_at** | **datetime** | Time when the object has been updated. Equals to _created_at_ if not updated after creation. | [optional] [readonly] 

## Example

```python
from ipam_federation.models.forward_looking_delegation import ForwardLookingDelegation

# TODO update the JSON string below
json = "{}"
# create an instance of ForwardLookingDelegation from a JSON string
forward_looking_delegation_instance = ForwardLookingDelegation.from_json(json)
# print the JSON string representation of the object
print(ForwardLookingDelegation.to_json())

# convert the object into a dict
forward_looking_delegation_dict = forward_looking_delegation_instance.to_dict()
# create an instance of ForwardLookingDelegation from a dict
forward_looking_delegation_from_dict = ForwardLookingDelegation.from_dict(forward_looking_delegation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


