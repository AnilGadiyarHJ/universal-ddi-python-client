# ipam_federation.AwsScopeTokenApi

All URIs are relative to *http://csp.infoblox.com/api/ddi/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**generate_token**](AwsScopeTokenApi.md#generate_token) | **POST** /federation/aws/scope/token | Generate AWS IPAM scope authentication token


# **generate_token**
> ManageScopeTokenResponse generate_token(body)

Generate AWS IPAM scope authentication token

Generate a time-limited JWT token for authenticating requests to the specified AWS IPAM scope

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
    api_instance = ipam_federation.AwsScopeTokenApi(api_client)
    body = ipam_federation.ManageScopeTokenRequest() # ManageScopeTokenRequest | 

    try:
        # Generate AWS IPAM scope authentication token
        api_response = api_instance.generate_token(body)
        pprint("The response of AwsScopeTokenApi->generate_token:\n")
        pprint(api_response)
    except Exception as e:
        pprint("Exception when calling AwsScopeTokenApi->generate_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**ManageScopeTokenRequest**](ManageScopeTokenRequest.md)|  | 

### Return type

[**ManageScopeTokenResponse**](ManageScopeTokenResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | POST operation response |  -  |
**400** | Invalid request parameters (e.g., malformed scope ARN, invalid expiration, missing required fields) |  -  |
**401** | Unauthorized access (e.g., invalid account ID, disabled account) |  -  |
**403** | Access denied to the specified AWS IPAM scope |  -  |
**404** | AWS IPAM scope or Infoblox account ID not found |  -  |
**500** | Internal server error occurred while generating token |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

