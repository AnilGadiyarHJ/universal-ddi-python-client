# ipam_federation.NextAvailableFederatedBlockApi

All URIs are relative to *http://csp.infoblox.com/api/ddi/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_next_available_federated_blocks**](NextAvailableFederatedBlockApi.md#create_next_available_federated_blocks) | **POST** /federation/federated_block/{id}/next_available_federated_block | Retrieve the next available federated block.
[**create_next_available_overlapping_blocks**](NextAvailableFederatedBlockApi.md#create_next_available_overlapping_blocks) | **POST** /federation/federated_block/{id}/next_available_overlapping_block | Retrieve the next available overlapping block.
[**list_next_available_federated_blocks**](NextAvailableFederatedBlockApi.md#list_next_available_federated_blocks) | **GET** /federation/federated_block/{id}/next_available_federated_block | List the next available federated block.


# **create_next_available_federated_blocks**
> CreateNextAvailableFederatedBlockResponse create_next_available_federated_blocks(id, body)

Retrieve the next available federated block.

Use this method to allocate the next available __FederatedBlock__ objects. This allocates one or more __FederatedBlock__ objects from the specified parent __FederatedBlock__ block.

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
    api_instance = ipam_federation.NextAvailableFederatedBlockApi(api_client)
    id = 'id_example' # str | An application specific resource identity of a resource
    body = ipam_federation.NextAvailableBlockRequest() # NextAvailableBlockRequest | 

    try:
        # Retrieve the next available federated block.
        api_response = api_instance.create_next_available_federated_blocks(id, body)
        pprint("The response of NextAvailableFederatedBlockApi->create_next_available_federated_blocks:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailableFederatedBlockApi->create_next_available_federated_blocks: %s\n" % e)
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

# **create_next_available_overlapping_blocks**
> CreateNextAvailableOverlappingBlockResponse create_next_available_overlapping_blocks(id, body)

Retrieve the next available overlapping block.

Use this method to allocate the next available __OverlappingBlock__ objects. This allocates one or more __OverlappingBlock__ objects from the specified parent __FederatedBlock__ block.

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
    api_instance = ipam_federation.NextAvailableFederatedBlockApi(api_client)
    id = 'id_example' # str | An application specific resource identity of a resource
    body = ipam_federation.NextAvailableBlockRequest() # NextAvailableBlockRequest | 

    try:
        # Retrieve the next available overlapping block.
        api_response = api_instance.create_next_available_overlapping_blocks(id, body)
        pprint("The response of NextAvailableFederatedBlockApi->create_next_available_overlapping_blocks:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailableFederatedBlockApi->create_next_available_overlapping_blocks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| An application specific resource identity of a resource | 
 **body** | [**NextAvailableBlockRequest**](NextAvailableBlockRequest.md)|  | 

### Return type

[**CreateNextAvailableOverlappingBlockResponse**](CreateNextAvailableOverlappingBlockResponse.md)

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

# **list_next_available_federated_blocks**
> ListNextAvailableFederatedBlockResponse list_next_available_federated_blocks(id, cidr=cidr, count=count, name=name, comment=comment)

List the next available federated block.

Use this method to retrieve the next available __FederatedBlock__ objects. This returns one or more __FederatedBlock__ objects from the specified parent __FederatedBlock__ block.

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
    api_instance = ipam_federation.NextAvailableFederatedBlockApi(api_client)
    id = 'id_example' # str | An application specific resource identity of a resource

    try:
        # List the next available federated block.
        api_response = api_instance.list_next_available_federated_blocks(id)
        pprint("The response of NextAvailableFederatedBlockApi->list_next_available_federated_blocks:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling NextAvailableFederatedBlockApi->list_next_available_federated_blocks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| An application specific resource identity of a resource | 
 **cidr** | **int**| The CIDR of the federated block. This is required, if _address_ does not specify it in its input. | [optional] 
 **count** | **int**| The count of __Block__ required. If not provided, it will default to 1. | [optional] 
 **name** | **str**| The name to be provided. | [optional] 
 **comment** | **str**| The description for the _federation/federated_block_. May contain 0 to 1024 characters. Can include UTF-8. | [optional] 

### Return type

[**ListNextAvailableFederatedBlockResponse**](ListNextAvailableFederatedBlockResponse.md)

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

