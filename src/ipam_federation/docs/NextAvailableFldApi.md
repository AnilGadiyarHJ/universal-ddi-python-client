# ipam_federation.NextAvailableFldApi

All URIs are relative to *http://csp.infoblox.com/api/ddi/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_next_available_fld**](NextAvailableFldApi.md#create_next_available_fld) | **POST** /federation/federated_block/{id}/create_next_available_fld | Create the next available __ForwardLookingDelegation__ objects within a specific __FederatedBlock__. Use this method to create the next available __ForwardLookingDelegation__ objects under the specified parent __FederatedBlock__.
[**create_next_available_fld_blocks**](NextAvailableFldApi.md#create_next_available_fld_blocks) | **POST** /federation/create_next_available_fld | Create the next available __ForwardLookingDelegation__ objects.
[**create_next_available_fld_for_pool**](NextAvailableFldApi.md#create_next_available_fld_for_pool) | **POST** /federation/federated_pool/{id}/create_next_available_fld | Create the next available __ForwardLookingDelegation__ objects within a pool.


# **create_next_available_fld**
> NextAvailableFLDResponse create_next_available_fld(id, body)

Create the next available __ForwardLookingDelegation__ objects within a specific __FederatedBlock__. Use this method to create the next available __ForwardLookingDelegation__ objects under the specified parent __FederatedBlock__.

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
    api_instance = ipam_federation.NextAvailableFldApi(api_client)
    id = 'id_example' # str | An application specific resource identity of a resource
    body = ipam_federation.CreateNextAvailableFLDRequestForBlock() # CreateNextAvailableFLDRequestForBlock | 

    try:
        # Create the next available __ForwardLookingDelegation__ objects within a specific __FederatedBlock__. Use this method to create the next available __ForwardLookingDelegation__ objects under the specified parent __FederatedBlock__.
        api_response = api_instance.create_next_available_fld(id, body)
        pprint("The response of NextAvailableFldApi->create_next_available_fld:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailableFldApi->create_next_available_fld: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| An application specific resource identity of a resource | 
 **body** | [**CreateNextAvailableFLDRequestForBlock**](CreateNextAvailableFLDRequestForBlock.md)|  | 

### Return type

[**NextAvailableFLDResponse**](NextAvailableFLDResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | POST operation response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_next_available_fld_blocks**
> NextAvailableFLDResponse create_next_available_fld_blocks(body)

Create the next available __ForwardLookingDelegation__ objects.

Use this method to create the next \"n\" available __ForwardLookingDelegation__ objects considering the parameter passed. The response will be \"n\" __ForwardLookingDelegation__ objects. A __ForwardLookingDelegation__ object (_federation/forward_looking_delegation_) is a set of contiguous IP addresses with no gap, expressed as a CIDR block. Forward Looking Delegations may be used to allocate unique space for future resources which will ultimately hold a Delegation for the same CIDR block.

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
    api_instance = ipam_federation.NextAvailableFldApi(api_client)
    body = ipam_federation.NextAvailableFLDRequest() # NextAvailableFLDRequest | 

    try:
        # Create the next available __ForwardLookingDelegation__ objects.
        api_response = api_instance.create_next_available_fld_blocks(body)
        pprint("The response of NextAvailableFldApi->create_next_available_fld_blocks:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailableFldApi->create_next_available_fld_blocks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**NextAvailableFLDRequest**](NextAvailableFLDRequest.md)|  | 

### Return type

[**NextAvailableFLDResponse**](NextAvailableFLDResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | POST operation response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_next_available_fld_for_pool**
> NextAvailableFLDResponse create_next_available_fld_for_pool(id, body)

Create the next available __ForwardLookingDelegation__ objects within a pool.

Use this method to allocate the next available __ForwardLookingDelegation__ objects within a specific federated pool. Federated blocks within the pool are evaluated in ascending CIDR order (largest address space first). Returns the allocated __ForwardLookingDelegation__ objects.

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
    api_instance = ipam_federation.NextAvailableFldApi(api_client)
    id = 'id_example' # str | An application specific resource identity of a resource
    body = ipam_federation.NextAvailableFLDPoolRequest() # NextAvailableFLDPoolRequest | 

    try:
        # Create the next available __ForwardLookingDelegation__ objects within a pool.
        api_response = api_instance.create_next_available_fld_for_pool(id, body)
        pprint("The response of NextAvailableFldApi->create_next_available_fld_for_pool:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailableFldApi->create_next_available_fld_for_pool: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| An application specific resource identity of a resource | 
 **body** | [**NextAvailableFLDPoolRequest**](NextAvailableFLDPoolRequest.md)|  | 

### Return type

[**NextAvailableFLDResponse**](NextAvailableFLDResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | POST operation response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

