# uncertainty_engine_resource_client.AccountRecordsApi

All URIs are relative to *https://tu8vus047g.execute-api.eu-west-2.amazonaws.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_account_record**](AccountRecordsApi.md#delete_account_record) | **DELETE** /api/accounts/{account_id} | Delete Account Record
[**get_account_record**](AccountRecordsApi.md#get_account_record) | **GET** /api/accounts/{account_id} | Get Account Record Id
[**get_account_record_projects**](AccountRecordsApi.md#get_account_record_projects) | **GET** /api/accounts/{account_id}/projects | Get Account Record Projects
[**post_account_record**](AccountRecordsApi.md#post_account_record) | **POST** /api/accounts | Post Account Record


# **delete_account_record**
> object delete_account_record(account_id)

Delete Account Record

Delete an account.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)


# Enter a context with an instance of the API client
async with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.AccountRecordsApi(api_client)
    account_id = 'account_id_example' # str | 

    try:
        # Delete Account Record
        api_response = await api_instance.delete_account_record(account_id)
        print("The response of AccountRecordsApi->delete_account_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountRecordsApi->delete_account_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**|  | 

### Return type

**object**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_record**
> AccountResponse get_account_record(account_id)

Get Account Record Id

Get a single account record.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.account_response import AccountResponse
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)


# Enter a context with an instance of the API client
async with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.AccountRecordsApi(api_client)
    account_id = 'account_id_example' # str | 

    try:
        # Get Account Record Id
        api_response = await api_instance.get_account_record(account_id)
        print("The response of AccountRecordsApi->get_account_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountRecordsApi->get_account_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**|  | 

### Return type

[**AccountResponse**](AccountResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_record_projects**
> GetAccountRecordProjectsResponse get_account_record_projects(account_id)

Get Account Record Projects

Get all projects for an account.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.get_account_record_projects_response import GetAccountRecordProjectsResponse
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)


# Enter a context with an instance of the API client
async with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.AccountRecordsApi(api_client)
    account_id = 'account_id_example' # str | 

    try:
        # Get Account Record Projects
        api_response = await api_instance.get_account_record_projects(account_id)
        print("The response of AccountRecordsApi->get_account_record_projects:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountRecordsApi->get_account_record_projects: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**|  | 

### Return type

[**GetAccountRecordProjectsResponse**](GetAccountRecordProjectsResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_account_record**
> AccountResponse post_account_record(post_account_record_request)

Post Account Record

Create a new account.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.account_response import AccountResponse
from uncertainty_engine_resource_client.models.post_account_record_request import PostAccountRecordRequest
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)


# Enter a context with an instance of the API client
async with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.AccountRecordsApi(api_client)
    post_account_record_request = uncertainty_engine_resource_client.PostAccountRecordRequest() # PostAccountRecordRequest | 

    try:
        # Post Account Record
        api_response = await api_instance.post_account_record(post_account_record_request)
        print("The response of AccountRecordsApi->post_account_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountRecordsApi->post_account_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **post_account_record_request** | [**PostAccountRecordRequest**](PostAccountRecordRequest.md)|  | 

### Return type

[**AccountResponse**](AccountResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

