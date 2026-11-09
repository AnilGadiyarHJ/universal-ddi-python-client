# ipam_federation.AwsScopeManagementApi

All URIs are relative to *http://csp.infoblox.com/api/ddi/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**scope_management**](AwsScopeManagementApi.md#scope_management) | **POST** /federation/aws/scope/management | Configure management settings for AWS IPAM scopes


# **scope_management**
> ScopeManagementResponse scope_management(body)

Configure management settings for AWS IPAM scopes

Enable or disable external management of an AWS IPAM scope by updating the federated realm's metadata to reflect the desired management mode

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
    api_instance = ipam_federation.AwsScopeManagementApi(api_client)
    body = ipam_federation.ScopeManagementObject() # ScopeManagementObject | Scope management configuration details

    try:
        # Configure management settings for AWS IPAM scopes
        api_response = api_instance.scope_management(body)
        pprint("The response of AwsScopeManagementApi->scope_management:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling AwsScopeManagementApi->scope_management: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ScopeManagementObject**](ScopeManagementObject.md)| Scope management configuration details | 

### Return type

[**ScopeManagementResponse**](ScopeManagementResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | POST operation response |  -  |
**400** | Bad Request - Invalid request parameters (e.g., malformed scope ARN, missing required fields) |  -  |
**401** | Unauthorized - Invalid or missing authentication token |  -  |
**404** | Not Found - AWS IPAM scope not found or does not exist |  -  |
**500** | Internal Server Error - An unexpected error occurred while setting scope management |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

