# ipam_federation.NextAppropriateDelegationApi

All URIs are relative to *http://csp.infoblox.com/api/ddi/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_next_appropriate_delegation**](NextAppropriateDelegationApi.md#create_next_appropriate_delegation) | **POST** /federation/next_appropriate_delegation | Create Next Appropriate Delegation


# **create_next_appropriate_delegation**
> NextAppropriateDelegationResponse create_next_appropriate_delegation(body)

Create Next Appropriate Delegation

Creates next appropriate __Delegation__ objects based on the provided payload. This method is used to generate a __Delegation__ that fits the specified criteria.

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
    api_instance = ipam_federation.NextAppropriateDelegationApi(api_client)
    body = ipam_federation.NextAppropriateDelegation() # NextAppropriateDelegation | The __NextAppropriateDelegation__ object.

    try:
        # Create Next Appropriate Delegation
        api_response = api_instance.create_next_appropriate_delegation(body)
        pprint("The response of NextAppropriateDelegationApi->create_next_appropriate_delegation:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAppropriateDelegationApi->create_next_appropriate_delegation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NextAppropriateDelegation**](NextAppropriateDelegation.md)| The __NextAppropriateDelegation__ object. | 

### Return type

[**NextAppropriateDelegationResponse**](NextAppropriateDelegationResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | POST operation response |  -  |
**400** | Invalid request parameters (e.g., missing required fields, missing required prerequisites, invalid address format, invalid CIDR values) |  -  |
**401** | Unauthorized access (e.g., invalid token) |  -  |
**404** | The resource referred to by &#39;scope_arn&#39; does not exist or is not found |  -  |
**409** | Not sufficient address space available to allocate for the request. |  -  |
**500** | Internal server error while allocating delegation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

