# NextAppropriateDelegation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cidr** | **int** | The CIDR Prefix Length of the required __Delegation__ object. This is a required field. | [optional] 
**count** | **int** | The count of the unique allocation with the provided CIDR. If not present then it will default to 1. | [optional] 
**delegated_to** | **str** | The identifier, which denotes as to whom the allocation would belong to. This field would take the format of &lt;provider_name&gt;://&lt;resource_to_be_assigned_to_id&gt;. Like for AWS, it will be aws://&lt;scope_arn&gt;. | [optional] 
**exclusions** | **List[str]** | The exclusions are the list of address prefixes (in the form of __IP_ADDRESS__/__CIDR__) which should be excluded while calculating for available allocations. This is an optional parameter. | [optional] 
**idempotency_key** | **str** | If the idempotency key is provided, a previously successful request using an identical key will be returned rather than being processed as an additional request. | [optional] 
**inclusions** | **List[str]** | The inclusions are the list of address prefixes (in the form of __IP_ADDRESS__/__CIDR__) which should be considered while calculating for available allocations. This is an optional parameter. | [optional] 
**name** | **str** | The name of the __Delegation__ object created. | [optional] 
**pool_id** | **str** | The unique identifier of the foreign __IPAM__ __Pool__ for which the request is being made, so that addresses appropriate for the __Pool__ may be selected. | [optional] 
**protocol** | **str** | The version of the address (_ip4_ or _ip6_). If not present then it will default to _ip4_. | [optional] 
**tags** | **object** | The tags for the __Delegation__ object created. It will be a JSON object. | [optional] 

## Example

```python
from ipam_federation.models.next_appropriate_delegation import NextAppropriateDelegation

# TODO update the JSON string below
json = "{}"
# create an instance of NextAppropriateDelegation from a JSON string
next_appropriate_delegation_instance = NextAppropriateDelegation.from_json(json)
# print the JSON string representation of the object
print(NextAppropriateDelegation.to_json())

# convert the object into a dict
next_appropriate_delegation_dict = next_appropriate_delegation_instance.to_dict()
# create an instance of NextAppropriateDelegation from a dict
next_appropriate_delegation_from_dict = NextAppropriateDelegation.from_dict(next_appropriate_delegation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


