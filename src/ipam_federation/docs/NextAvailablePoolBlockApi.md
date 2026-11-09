# ipam_federation.NextAvailablePoolBlockApi

All URIs are relative to *http://csp.infoblox.com/api/ddi/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_next_available_blocks**](NextAvailablePoolBlockApi.md#create_next_available_blocks) | **POST** /federation/federated_pool/{id}/next_available_federated_block | Create the next available federated blocks within a pool.


# **create_next_available_blocks**
> CreateNextAvailableFederatedBlockResponse create_next_available_blocks(id, body)

Create the next available federated blocks within a pool.

Use this method to allocate the next available __FederatedBlock__ objects within a specific federated pool. This allocates one or more __FederatedBlock__ objects from the specified federated pool. This is a thin wrapper that reuses the block-level NAB logic by finding suitable parent blocks in the pool.

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
    api_instance = ipam_federation.NextAvailablePoolBlockApi(api_client)
    id = 'id_example' # str | An application specific resource identity of a resource
    body = ipam_federation.NextAvailableBlockRequest() # NextAvailableBlockRequest | 

    try:
        # Create the next available federated blocks within a pool.
        api_response = api_instance.create_next_available_blocks(id, body)
        pprint("The response of NextAvailablePoolBlockApi->create_next_available_blocks:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailablePoolBlockApi->create_next_available_blocks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| An application specific resource identity of a resource | 
 **body** | [**NextAvailableBlockRequest**](NextAvailableBlockRequest.md)|  | 

### Return type

[**CreateNextAvailableFederatedBlockResponse**](CreateNextAvailableFederatedBlockResponse.md)

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

