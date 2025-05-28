# uncertainty_engine_resource_client.ProjectRecordsApi

All URIs are relative to *https://tu8vus047g.execute-api.eu-west-2.amazonaws.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_project_record**](ProjectRecordsApi.md#delete_project_record) | **DELETE** /api/projects/{project_id} | Delete Project Record
[**get_project_record_id**](ProjectRecordsApi.md#get_project_record_id) | **GET** /api/projects/{project_id} | Get Project Record Id
[**patch_project_record**](ProjectRecordsApi.md#patch_project_record) | **PATCH** /api/projects/{project_id}/name | Patch Project Record Name
[**post_project_record**](ProjectRecordsApi.md#post_project_record) | **POST** /api/projects | Post Project Record


# **delete_project_record**
> object delete_project_record(project_id)

Delete Project Record

Delete a project using the project id.

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
with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.ProjectRecordsApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Delete Project Record
        api_response = api_instance.delete_project_record(project_id)
        print("The response of ProjectRecordsApi->delete_project_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectRecordsApi->delete_project_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

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

# **get_project_record_id**
> ProjectResponse get_project_record_id(project_id)

Get Project Record Id

Get a single project using the project id.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.project_response import ProjectResponse
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)


# Enter a context with an instance of the API client
with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.ProjectRecordsApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get Project Record Id
        api_response = api_instance.get_project_record_id(project_id)
        print("The response of ProjectRecordsApi->get_project_record_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectRecordsApi->get_project_record_id: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**ProjectResponse**](ProjectResponse.md)

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

# **patch_project_record**
> ProjectResponse patch_project_record(project_id, patch_project_record_name_request)

Patch Project Record Name

Rename an existing project.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.patch_project_record_name_request import PatchProjectRecordNameRequest
from uncertainty_engine_resource_client.models.project_response import ProjectResponse
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)


# Enter a context with an instance of the API client
with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.ProjectRecordsApi(api_client)
    project_id = 'project_id_example' # str | 
    patch_project_record_name_request = uncertainty_engine_resource_client.PatchProjectRecordNameRequest() # PatchProjectRecordNameRequest | 

    try:
        # Patch Project Record Name
        api_response = api_instance.patch_project_record(project_id, patch_project_record_name_request)
        print("The response of ProjectRecordsApi->patch_project_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectRecordsApi->patch_project_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **patch_project_record_name_request** | [**PatchProjectRecordNameRequest**](PatchProjectRecordNameRequest.md)|  | 

### Return type

[**ProjectResponse**](ProjectResponse.md)

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

# **post_project_record**
> ProjectResponse post_project_record(post_project_record_request)

Post Project Record

Create a new project.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.post_project_record_request import PostProjectRecordRequest
from uncertainty_engine_resource_client.models.project_response import ProjectResponse
from uncertainty_engine_resource_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://tu8vus047g.execute-api.eu-west-2.amazonaws.com
# See configuration.py for a list of all supported configuration parameters.
configuration = uncertainty_engine_resource_client.Configuration(
    host = "https://tu8vus047g.execute-api.eu-west-2.amazonaws.com"
)


# Enter a context with an instance of the API client
with uncertainty_engine_resource_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = uncertainty_engine_resource_client.ProjectRecordsApi(api_client)
    post_project_record_request = uncertainty_engine_resource_client.PostProjectRecordRequest() # PostProjectRecordRequest | 

    try:
        # Post Project Record
        api_response = api_instance.post_project_record(post_project_record_request)
        print("The response of ProjectRecordsApi->post_project_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ProjectRecordsApi->post_project_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **post_project_record_request** | [**PostProjectRecordRequest**](PostProjectRecordRequest.md)|  | 

### Return type

[**ProjectResponse**](ProjectResponse.md)

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

