# uncertainty_engine_resource_client.AuthApi

All URIs are relative to *https://tu8vus047g.execute-api.eu-west-2.amazonaws.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_tokens**](AuthApi.md#get_tokens) | **POST** /api/auth/token | Get Tokens
[**refresh_token**](AuthApi.md#refresh_token) | **POST** /api/auth/refresh | Refresh Token


# **get_tokens**
> TokenResponse get_tokens()

Get Tokens

Exchange Cognito tokens for API tokens

### Example

* Bearer Authentication (HTTPBearer):

```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.token_response import TokenResponse
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: HTTPBearer
configuration = uncertainty_engine_resource_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
async with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.AuthApi(api_client)

    try:
        # Get Tokens
        api_response = await api_instance.get_tokens()
        print("The response of AuthApi->get_tokens:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->get_tokens: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **refresh_token**
> TokenResponse refresh_token()

Refresh Token

Get new access token using refresh token

### Example

* Bearer Authentication (HTTPBearer):

```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.token_response import TokenResponse
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: HTTPBearer
configuration = uncertainty_engine_resource_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
async with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.AuthApi(api_client)

    try:
        # Refresh Token
        api_response = await api_instance.refresh_token()
        print("The response of AuthApi->refresh_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AuthApi->refresh_token: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

