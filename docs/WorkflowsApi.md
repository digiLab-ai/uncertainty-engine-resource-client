# uncertainty_engine_resource_client.WorkflowsApi

All URIs are relative to *https://tu8vus047g.execute-api.eu-west-2.amazonaws.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_workflow_record**](WorkflowsApi.md#delete_workflow_record) | **DELETE** /api/projects/{project_id}/workflows/{workflow_id} | Delete Workflow
[**delete_workflow_version_record**](WorkflowsApi.md#delete_workflow_version_record) | **DELETE** /api/projects/{project_id}/workflows/{workflow_id}/versions/{workflow_version_id} | Delete Workflow Version
[**get_latest_workflow_version**](WorkflowsApi.md#get_latest_workflow_version) | **GET** /api/projects/{project_id}/workflows/{workflow_id}/latest | Get Latest Workflow Version
[**get_project_workflow_records**](WorkflowsApi.md#get_project_workflow_records) | **GET** /api/projects/{project_id}/workflows | Get Project Workflow Records
[**get_workflow_record**](WorkflowsApi.md#get_workflow_record) | **GET** /api/projects/{project_id}/workflows/{workflow_id} | Get Workflow Record
[**get_workflow_version**](WorkflowsApi.md#get_workflow_version) | **GET** /api/projects/{project_id}/workflows/{workflow_id}/versions/{workflow_version_id} | Get Workflow Version
[**get_workflow_version_records**](WorkflowsApi.md#get_workflow_version_records) | **GET** /api/projects/{project_id}/workflows/{workflow_id}/versions | Get Workflow Version Records
[**post_workflow_record**](WorkflowsApi.md#post_workflow_record) | **POST** /api/projects/{project_id}/workflows | Post Workflow Record
[**post_workflow_version**](WorkflowsApi.md#post_workflow_version) | **POST** /api/projects/{project_id}/workflows/{workflow_id}/versions | Post Workflow Version
[**put_workflow_version**](WorkflowsApi.md#put_workflow_version) | **PUT** /api/projects/{project_id}/workflows/{workflow_id}/versions/{workflow_version_id} | Put Workflow Version


# **delete_workflow_record**
> object delete_workflow_record(project_id, workflow_id)

Delete Workflow

Delete a workflow (including all versions) using the workflow id.

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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 

    try:
        # Delete Workflow
        api_response = api_instance.delete_workflow_record(project_id, workflow_id)
        print("The response of WorkflowsApi->delete_workflow_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->delete_workflow_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 

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

# **delete_workflow_version_record**
> object delete_workflow_version_record(project_id, workflow_id, workflow_version_id)

Delete Workflow Version

Delete a workflow version using the version id.

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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 
    workflow_version_id = 'workflow_version_id_example' # str | 

    try:
        # Delete Workflow Version
        api_response = api_instance.delete_workflow_version_record(project_id, workflow_id, workflow_version_id)
        print("The response of WorkflowsApi->delete_workflow_version_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->delete_workflow_version_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 
 **workflow_version_id** | **str**|  | 

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

# **get_latest_workflow_version**
> WorkflowVersionResponse get_latest_workflow_version(project_id, workflow_id)

Get Latest Workflow Version

Get the most recent workflow version for a workflow.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.workflow_version_response import WorkflowVersionResponse
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 

    try:
        # Get Latest Workflow Version
        api_response = api_instance.get_latest_workflow_version(project_id, workflow_id)
        print("The response of WorkflowsApi->get_latest_workflow_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->get_latest_workflow_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 

### Return type

[**WorkflowVersionResponse**](WorkflowVersionResponse.md)

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

# **get_project_workflow_records**
> GetWorkflowRecordsResponse get_project_workflow_records(project_id)

Get Project Workflow Records

Get all workflow records for a project.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.get_workflow_records_response import GetWorkflowRecordsResponse
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 

    try:
        # Get Project Workflow Records
        api_response = api_instance.get_project_workflow_records(project_id)
        print("The response of WorkflowsApi->get_project_workflow_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->get_project_workflow_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 

### Return type

[**GetWorkflowRecordsResponse**](GetWorkflowRecordsResponse.md)

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

# **get_workflow_record**
> WorkflowResponse get_workflow_record(project_id, workflow_id)

Get Workflow Record

Get a single workflow from a project.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.workflow_response import WorkflowResponse
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 

    try:
        # Get Workflow Record
        api_response = api_instance.get_workflow_record(project_id, workflow_id)
        print("The response of WorkflowsApi->get_workflow_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->get_workflow_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 

### Return type

[**WorkflowResponse**](WorkflowResponse.md)

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

# **get_workflow_version**
> WorkflowVersionResponse get_workflow_version(project_id, workflow_id, workflow_version_id)

Get Workflow Version

Get a single workflow version from a workflow.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.workflow_version_response import WorkflowVersionResponse
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 
    workflow_version_id = 'workflow_version_id_example' # str | 

    try:
        # Get Workflow Version
        api_response = api_instance.get_workflow_version(project_id, workflow_id, workflow_version_id)
        print("The response of WorkflowsApi->get_workflow_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->get_workflow_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 
 **workflow_version_id** | **str**|  | 

### Return type

[**WorkflowVersionResponse**](WorkflowVersionResponse.md)

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

# **get_workflow_version_records**
> GetWorkflowVersionRecordsResponse get_workflow_version_records(project_id, workflow_id)

Get Workflow Version Records

Get all workflow version records for a workflow.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.get_workflow_version_records_response import GetWorkflowVersionRecordsResponse
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 

    try:
        # Get Workflow Version Records
        api_response = api_instance.get_workflow_version_records(project_id, workflow_id)
        print("The response of WorkflowsApi->get_workflow_version_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->get_workflow_version_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 

### Return type

[**GetWorkflowVersionRecordsResponse**](GetWorkflowVersionRecordsResponse.md)

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

# **post_workflow_record**
> WorkflowResponse post_workflow_record(project_id, post_workflow_record_request)

Post Workflow Record

Create a new workflow record.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.post_workflow_record_request import PostWorkflowRecordRequest
from uncertainty_engine_resource_client.models.workflow_response import WorkflowResponse
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    post_workflow_record_request = uncertainty_engine_resource_client.PostWorkflowRecordRequest() # PostWorkflowRecordRequest | 

    try:
        # Post Workflow Record
        api_response = api_instance.post_workflow_record(project_id, post_workflow_record_request)
        print("The response of WorkflowsApi->post_workflow_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->post_workflow_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **post_workflow_record_request** | [**PostWorkflowRecordRequest**](PostWorkflowRecordRequest.md)|  | 

### Return type

[**WorkflowResponse**](WorkflowResponse.md)

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

# **post_workflow_version**
> WorkflowVersionResponse post_workflow_version(project_id, workflow_id, post_workflow_version_request)

Post Workflow Version

Create a new workflow version.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.post_workflow_version_request import PostWorkflowVersionRequest
from uncertainty_engine_resource_client.models.workflow_version_response import WorkflowVersionResponse
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 
    post_workflow_version_request = uncertainty_engine_resource_client.PostWorkflowVersionRequest() # PostWorkflowVersionRequest | 

    try:
        # Post Workflow Version
        api_response = api_instance.post_workflow_version(project_id, workflow_id, post_workflow_version_request)
        print("The response of WorkflowsApi->post_workflow_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->post_workflow_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 
 **post_workflow_version_request** | [**PostWorkflowVersionRequest**](PostWorkflowVersionRequest.md)|  | 

### Return type

[**WorkflowVersionResponse**](WorkflowVersionResponse.md)

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

# **put_workflow_version**
> object put_workflow_version(project_id, workflow_id, workflow_version_id, update_workflow_version_request)

Put Workflow Version

Update a workflow version. Can update either the workflow content, the version record metadata, or both.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.update_workflow_version_request import UpdateWorkflowVersionRequest
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
    api_instance = uncertainty_engine_resource_client.WorkflowsApi(api_client)
    project_id = 'project_id_example' # str | 
    workflow_id = 'workflow_id_example' # str | 
    workflow_version_id = 'workflow_version_id_example' # str | 
    update_workflow_version_request = uncertainty_engine_resource_client.UpdateWorkflowVersionRequest() # UpdateWorkflowVersionRequest | 

    try:
        # Put Workflow Version
        api_response = api_instance.put_workflow_version(project_id, workflow_id, workflow_version_id, update_workflow_version_request)
        print("The response of WorkflowsApi->put_workflow_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WorkflowsApi->put_workflow_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **workflow_id** | **str**|  | 
 **workflow_version_id** | **str**|  | 
 **update_workflow_version_request** | [**UpdateWorkflowVersionRequest**](UpdateWorkflowVersionRequest.md)|  | 

### Return type

**object**

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

