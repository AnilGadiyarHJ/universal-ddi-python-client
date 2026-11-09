# CreateNextAvailableFLDRequestForBlock

Use this request to create the next available __ForwardLookingDelegation__ objects within a specific parent __FederatedBlock__.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cidr** | **int** | The CIDR of the __ForwardLookingDelegation__. This is required. | 
**comment** | **str** | The description for the __ForwardLookingDelegation__. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
**count** | **int** | The count of __ForwardLookingDelegation__ required. If not provided, it will default to 1. | [optional] 
**id** | **str** | The resource identifier. | [readonly] 
**name** | **str** | The name to be provided. | [optional] 
**tags** | **object** | The tags for the __ForwardLookingDelegation__ in JSON format. | [optional] 

## Example

```python
from ipam_federation.models.create_next_available_fld_request_for_block import CreateNextAvailableFLDRequestForBlock

# TODO update the JSON string below
json = "{}"
# create an instance of CreateNextAvailableFLDRequestForBlock from a JSON string
create_next_available_fld_request_for_block_instance = CreateNextAvailableFLDRequestForBlock.from_json(json)
# print the JSON string representation of the object
print(CreateNextAvailableFLDRequestForBlock.to_json())

# convert the object into a dict
create_next_available_fld_request_for_block_dict = create_next_available_fld_request_for_block_instance.to_dict()
# create an instance of CreateNextAvailableFLDRequestForBlock from a dict
create_next_available_fld_request_for_block_from_dict = CreateNextAvailableFLDRequestForBlock.from_dict(create_next_available_fld_request_for_block_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


