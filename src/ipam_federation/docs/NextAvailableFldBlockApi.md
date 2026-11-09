# ipam_federation.NextAvailableFldBlockApi

All URIs are relative to *http://csp.infoblox.com/api/ddi/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_next_available_fld_blocks**](NextAvailableFldBlockApi.md#list_next_available_fld_blocks) | **GET** /federation/list_next_available_fld | List the next available __ForwardLookingDelegation__ objects.


# **list_next_available_fld_blocks**
> NextAvailableFLDResponse list_next_available_fld_blocks(cidr=cidr, count=count, name=name, comment=comment, protocol=protocol)

List the next available __ForwardLookingDelegation__ objects.

Use this method to get the next \"n\" available __ForwardLookingDelegation__ objects which can be created considering the parameter passed. The response will be \"n\" __ForwardLookingDelegation__ objects. A __ForwardLookingDelegation__ object (_federation/forward_looking_delegation_) is a set of contiguous IP addresses with no gap, expressed as a CIDR block. Forward Looking Delegations may be used to allocate unique space for future resources which will ultimately hold a Delegation for the same CIDR block.

### Example

* Api Key Authentication (ApiKeyAuth):
```python
import os
from pprint import pprint

import ipam_federation

from universal_ddi_client.api_client import ApiClient
from universal_ddi_client.configuration import Configuration

# Defining the Portal URL is optional and defaults to "https://csp.infoblox.com"
# See configuration.py for a list of all supported configuration parameters.
configuration = Configuration(
    portal_url = os.getenv('INFOBLOX_PORTAL_URL'),
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.

# Configure Portal key authorization: ApiKeyAuth
configuration.portal_key = os.getenv("INFOBLOX_PORTAL_KEY")

# Enter a context with an instance of the API client
with ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = ipam_federation.NextAvailableFldBlockApi(api_client)

    try:
        # List the next available __ForwardLookingDelegation__ objects.
        api_response = api_instance.list_next_available_fld_blocks()
        pprint("The response of NextAvailableFldBlockApi->list_next_available_fld_blocks:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailableFldBlockApi->list_next_available_fld_blocks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **cidr** | **int**| The CIDR of the __ForwardLookingDelegation__. This is required. | [optional] 
 **count** | **int**| The count of __ForwardLookingDelegation__ required. If not provided, it will default to 1. | [optional] 
 **name** | **str**| The name to be provided. | [optional] 
 **comment** | **str**| The description for the __ForwardLookingDelegation__. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 
 **protocol** | **str**| The version of the address (_ip4_ or _ip6_). If not present then it will default to _ip4_. | [optional] 

### Return type

[**NextAvailableFLDResponse**](NextAvailableFLDResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | GET operation response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

