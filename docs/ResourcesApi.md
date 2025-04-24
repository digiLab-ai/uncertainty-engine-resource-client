# uncertainty_engine_resource_client.ResourcesApi

All URIs are relative to *https://tu8vus047g.execute-api.eu-west-2.amazonaws.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_resource_record**](ResourcesApi.md#delete_resource_record) | **DELETE** /api/projects/{project_id}/resources/{resource_type}/{resource_id} | Delete Resource
[**delete_resource_version_record**](ResourcesApi.md#delete_resource_version_record) | **DELETE** /api/projects/{project_id}/resources/{resource_type}/{resource_id}/versions/{resource_version_id} | Delete Resource Version
[**get_latest_resource_version**](ResourcesApi.md#get_latest_resource_version) | **GET** /api/projects/{project_id}/resources/{resource_type}/{resource_id}/latest | Get Latest Resource Version
[**get_project_resource_records**](ResourcesApi.md#get_project_resource_records) | **GET** /api/projects/{project_id}/resources/{resource_type} | Get Project Resource Records
[**get_resource_record**](ResourcesApi.md#get_resource_record) | **GET** /api/projects/{project_id}/resources/{resource_type}/{resource_id} | Get Resource Record
[**get_resource_version**](ResourcesApi.md#get_resource_version) | **GET** /api/projects/{project_id}/resources/{resource_type}/{resource_id}/versions/{resource_version_id} | Get Resource Version
[**get_resource_version_records**](ResourcesApi.md#get_resource_version_records) | **GET** /api/projects/{project_id}/resources/{resource_type}/{resource_id}/versions | Get Resource Version Records
[**patch_resource_version**](ResourcesApi.md#patch_resource_version) | **PATCH** /api/projects/{project_id}/resources/{resource_type}/{resource_id}/versions/{resource_version_id} | Patch Resource Version
[**post_resource_record**](ResourcesApi.md#post_resource_record) | **POST** /api/projects/{project_id}/resources/{resource_type} | Post Resource Record
[**post_resource_version**](ResourcesApi.md#post_resource_version) | **POST** /api/projects/{project_id}/resources/{resource_type}/{resource_id}/versions | Post Resource Version
[**put_upload_resource_version**](ResourcesApi.md#put_upload_resource_version) | **PUT** /api/projects/{project_id}/resources/{resource_type}/{resource_id}/pending/{pending_record_id} | Put Upload Resource Version


# **delete_resource_record**
> object delete_resource_record(project_id, resource_type, resource_id)

Delete Resource

Delete a resource (including all versions) using the resource id.

This endpoint deletes the resource record and all of its versions from the database.
It will also delete all of the actual resources from cloud storage.

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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 

    try:
        # Delete Resource
        api_response = api_instance.delete_resource_record(project_id, resource_type, resource_id)
        print("The response of ResourcesApi->delete_resource_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->delete_resource_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 

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

# **delete_resource_version_record**
> object delete_resource_version_record(project_id, resource_type, resource_id, resource_version_id)

Delete Resource Version

Delete a resource version using the version id.

This endpoint deletes the resource version record and the actual resource from cloud storage.
It will also update the resource record to remove the version id from the list of versions.

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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 
    resource_version_id = 'resource_version_id_example' # str | 

    try:
        # Delete Resource Version
        api_response = api_instance.delete_resource_version_record(project_id, resource_type, resource_id, resource_version_id)
        print("The response of ResourcesApi->delete_resource_version_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->delete_resource_version_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 
 **resource_version_id** | **str**|  | 

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

# **get_latest_resource_version**
> GetResourceVersionResponse get_latest_resource_version(project_id, resource_type, resource_id)

Get Latest Resource Version

Get the most recent version of a resource.
This endpoint returns the most recent version of a resource, along with its metadata.
The resource version record contains information about the version, such as its ID, name, and etc.
The resource its self is returned as a presigned GET URL.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.get_resource_version_response import GetResourceVersionResponse
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 

    try:
        # Get Latest Resource Version
        api_response = api_instance.get_latest_resource_version(project_id, resource_type, resource_id)
        print("The response of ResourcesApi->get_latest_resource_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->get_latest_resource_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 

### Return type

[**GetResourceVersionResponse**](GetResourceVersionResponse.md)

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

# **get_project_resource_records**
> GetResourceRecordsResponse get_project_resource_records(project_id, resource_type)

Get Project Resource Records

Get all resource records within a project.

This endpoint returns all of the resource records, of a certain resource type, within a given project.
The records contain metadata about the resources, such as their IDs, names, and etc. This record also contains
a list of version IDs for each resource. These IDs can be used to retrieve the actual resource versions.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.get_resource_records_response import GetResourceRecordsResponse
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 

    try:
        # Get Project Resource Records
        api_response = api_instance.get_project_resource_records(project_id, resource_type)
        print("The response of ResourcesApi->get_project_resource_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->get_project_resource_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 

### Return type

[**GetResourceRecordsResponse**](GetResourceRecordsResponse.md)

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

# **get_resource_record**
> ResourceResponse get_resource_record(project_id, resource_type, resource_id)

Get Resource Record

Get a single resource within a project.

This record contain metadata about the resource, such as it's ID, name, etc. This record also contains
a list of version IDs; these IDs can be used to retrieve the actual resource versions.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.resource_response import ResourceResponse
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 

    try:
        # Get Resource Record
        api_response = api_instance.get_resource_record(project_id, resource_type, resource_id)
        print("The response of ResourcesApi->get_resource_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->get_resource_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 

### Return type

[**ResourceResponse**](ResourceResponse.md)

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

# **get_resource_version**
> GetResourceVersionResponse get_resource_version(project_id, resource_type, resource_id, resource_version_id)

Get Resource Version

Get a single resource version from a resource.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.get_resource_version_response import GetResourceVersionResponse
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 
    resource_version_id = 'resource_version_id_example' # str | 

    try:
        # Get Resource Version
        api_response = api_instance.get_resource_version(project_id, resource_type, resource_id, resource_version_id)
        print("The response of ResourcesApi->get_resource_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->get_resource_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 
 **resource_version_id** | **str**|  | 

### Return type

[**GetResourceVersionResponse**](GetResourceVersionResponse.md)

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

# **get_resource_version_records**
> GetResourceVersionRecordsResponse get_resource_version_records(project_id, resource_type, resource_id)

Get Resource Version Records

Get all resource version records for a resource.

This endpoint returns all of the resource version records for a given resource.
The records contain metadata about the resource versions, such as their IDs, names, and etc.
These records also contain the location of the resource versions in cloud storage.
This can be useful for debugging and auditing purposes.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.get_resource_version_records_response import GetResourceVersionRecordsResponse
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 

    try:
        # Get Resource Version Records
        api_response = api_instance.get_resource_version_records(project_id, resource_type, resource_id)
        print("The response of ResourcesApi->get_resource_version_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->get_resource_version_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 

### Return type

[**GetResourceVersionRecordsResponse**](GetResourceVersionRecordsResponse.md)

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

# **patch_resource_version**
> object patch_resource_version(project_id, resource_type, resource_id, resource_version_id, patch_resource_version_request)

Patch Resource Version

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.patch_resource_version_request import PatchResourceVersionRequest
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 
    resource_version_id = 'resource_version_id_example' # str | 
    patch_resource_version_request = uncertainty_engine_resource_client.PatchResourceVersionRequest() # PatchResourceVersionRequest | 

    try:
        # Patch Resource Version
        api_response = api_instance.patch_resource_version(project_id, resource_type, resource_id, resource_version_id, patch_resource_version_request)
        print("The response of ResourcesApi->patch_resource_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->patch_resource_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 
 **resource_version_id** | **str**|  | 
 **patch_resource_version_request** | [**PatchResourceVersionRequest**](PatchResourceVersionRequest.md)|  | 

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

# **post_resource_record**
> ResourceResponse post_resource_record(project_id, resource_type, post_resource_record_request)

Post Resource Record

Create a new resource record.

This record contains all of the metadata about a resource but not the resource itself.
This is to allow for versioning (were each version is associated with an actual resource, e.g csv, file, model, ...).
Before creating a version of a resource, the resource record must be created.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.post_resource_record_request import PostResourceRecordRequest
from uncertainty_engine_resource_client.models.resource_response import ResourceResponse
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    post_resource_record_request = uncertainty_engine_resource_client.PostResourceRecordRequest() # PostResourceRecordRequest | 

    try:
        # Post Resource Record
        api_response = api_instance.post_resource_record(project_id, resource_type, post_resource_record_request)
        print("The response of ResourcesApi->post_resource_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->post_resource_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **post_resource_record_request** | [**PostResourceRecordRequest**](PostResourceRecordRequest.md)|  | 

### Return type

[**ResourceResponse**](ResourceResponse.md)

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

# **post_resource_version**
> PostResourceVersionResponse post_resource_version(project_id, resource_type, resource_id, post_resource_version_request)

Post Resource Version

Initiate the upload of a resource version to the cloud storage.
This endpoint creates a `pending_version_resource_record`.
It returns a signed URL and `pending_record_id`.
The client should use the presigned URL to upload the large resource and then call the `PUT` endpoint to complete the upload.

### Example


```python
import uncertainty_engine_resource_client
from uncertainty_engine_resource_client.models.post_resource_version_request import PostResourceVersionRequest
from uncertainty_engine_resource_client.models.post_resource_version_response import PostResourceVersionResponse
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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 
    post_resource_version_request = uncertainty_engine_resource_client.PostResourceVersionRequest() # PostResourceVersionRequest | 

    try:
        # Post Resource Version
        api_response = api_instance.post_resource_version(project_id, resource_type, resource_id, post_resource_version_request)
        print("The response of ResourcesApi->post_resource_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->post_resource_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 
 **post_resource_version_request** | [**PostResourceVersionRequest**](PostResourceVersionRequest.md)|  | 

### Return type

[**PostResourceVersionResponse**](PostResourceVersionResponse.md)

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

# **put_upload_resource_version**
> object put_upload_resource_version(project_id, resource_type, resource_id, pending_record_id)

Put Upload Resource Version

Complete the upload of a resource version to the cloud storage.

This will convert a `pending_version_resource_record` to a `resource_version_record`.
It will also update the resource record to include the new version id.
The client should call this endpoint after uploading the resource to the presigned URL.
If this endpoint is not called, the resource version will be deleted after a certain period of time.
If this endpoint is called and the expected resource is not found, the resource version will be deleted and
an error will be raised.

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
    api_instance = uncertainty_engine_resource_client.ResourcesApi(api_client)
    project_id = 'project_id_example' # str | 
    resource_type = 'resource_type_example' # str | 
    resource_id = 'resource_id_example' # str | 
    pending_record_id = 'pending_record_id_example' # str | 

    try:
        # Put Upload Resource Version
        api_response = api_instance.put_upload_resource_version(project_id, resource_type, resource_id, pending_record_id)
        print("The response of ResourcesApi->put_upload_resource_version:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->put_upload_resource_version: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **project_id** | **str**|  | 
 **resource_type** | **str**|  | 
 **resource_id** | **str**|  | 
 **pending_record_id** | **str**|  | 

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

