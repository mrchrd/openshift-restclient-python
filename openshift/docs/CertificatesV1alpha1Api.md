# openshift.client.CertificatesV1alpha1Api

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_certificate_signing_request**](CertificatesV1alpha1Api.md#create_certificate_signing_request) | **POST** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests | 
[**delete_certificate_signing_request**](CertificatesV1alpha1Api.md#delete_certificate_signing_request) | **DELETE** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests/{name} | 
[**delete_collection_certificate_signing_request**](CertificatesV1alpha1Api.md#delete_collection_certificate_signing_request) | **DELETE** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests | 
[**get_api_resources**](CertificatesV1alpha1Api.md#get_api_resources) | **GET** /apis/certificates.k8s.io/v1alpha1/ | 
[**list_certificate_signing_request**](CertificatesV1alpha1Api.md#list_certificate_signing_request) | **GET** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests | 
[**patch_certificate_signing_request**](CertificatesV1alpha1Api.md#patch_certificate_signing_request) | **PATCH** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests/{name} | 
[**read_certificate_signing_request**](CertificatesV1alpha1Api.md#read_certificate_signing_request) | **GET** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests/{name} | 
[**replace_certificate_signing_request**](CertificatesV1alpha1Api.md#replace_certificate_signing_request) | **PUT** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests/{name} | 
[**replace_certificate_signing_request_approval**](CertificatesV1alpha1Api.md#replace_certificate_signing_request_approval) | **PUT** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests/{name}/approval | 
[**replace_certificate_signing_request_status**](CertificatesV1alpha1Api.md#replace_certificate_signing_request_status) | **PUT** /apis/certificates.k8s.io/v1alpha1/certificatesigningrequests/{name}/status | 


# **create_certificate_signing_request**
> V1alpha1CertificateSigningRequest create_certificate_signing_request(body, pretty=pretty)



create a CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
body = openshift.client.V1alpha1CertificateSigningRequest() # V1alpha1CertificateSigningRequest | 
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)

try: 
    api_response = api_instance.create_certificate_signing_request(body, pretty=pretty)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->create_certificate_signing_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)|  | 
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 

### Return type

[**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_certificate_signing_request**
> UnversionedStatus delete_certificate_signing_request(name, body, pretty=pretty, grace_period_seconds=grace_period_seconds, orphan_dependents=orphan_dependents)



delete a CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
name = 'name_example' # str | name of the CertificateSigningRequest
body = openshift.client.V1DeleteOptions() # V1DeleteOptions | 
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)
grace_period_seconds = 56 # int | The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. (optional)
orphan_dependents = true # bool | Should the dependent objects be orphaned. If true/false, the \"orphan\" finalizer will be added to/removed from the object's finalizers list. (optional)

try: 
    api_response = api_instance.delete_certificate_signing_request(name, body, pretty=pretty, grace_period_seconds=grace_period_seconds, orphan_dependents=orphan_dependents)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->delete_certificate_signing_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| name of the CertificateSigningRequest | 
 **body** | [**V1DeleteOptions**](V1DeleteOptions.md)|  | 
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **grace_period_seconds** | **int**| The duration in seconds before the object should be deleted. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately. | [optional] 
 **orphan_dependents** | **bool**| Should the dependent objects be orphaned. If true/false, the \&quot;orphan\&quot; finalizer will be added to/removed from the object&#39;s finalizers list. | [optional] 

### Return type

[**UnversionedStatus**](UnversionedStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_collection_certificate_signing_request**
> UnversionedStatus delete_collection_certificate_signing_request(pretty=pretty, field_selector=field_selector, label_selector=label_selector, resource_version=resource_version, timeout_seconds=timeout_seconds, watch=watch)



delete collection of CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)
field_selector = 'field_selector_example' # str | A selector to restrict the list of returned objects by their fields. Defaults to everything. (optional)
label_selector = 'label_selector_example' # str | A selector to restrict the list of returned objects by their labels. Defaults to everything. (optional)
resource_version = 'resource_version_example' # str | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. (optional)
timeout_seconds = 56 # int | Timeout for the list/watch call. (optional)
watch = true # bool | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. (optional)

try: 
    api_response = api_instance.delete_collection_certificate_signing_request(pretty=pretty, field_selector=field_selector, label_selector=label_selector, resource_version=resource_version, timeout_seconds=timeout_seconds, watch=watch)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->delete_collection_certificate_signing_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **field_selector** | **str**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] 
 **label_selector** | **str**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] 
 **resource_version** | **str**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. | [optional] 
 **timeout_seconds** | **int**| Timeout for the list/watch call. | [optional] 
 **watch** | **bool**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. | [optional] 

### Return type

[**UnversionedStatus**](UnversionedStatus.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_api_resources**
> UnversionedAPIResourceList get_api_resources()



get available resources

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()

try: 
    api_response = api_instance.get_api_resources()
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->get_api_resources: %s\n" % e)
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**UnversionedAPIResourceList**](UnversionedAPIResourceList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json, application/yaml, application/vnd.kubernetes.protobuf
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_certificate_signing_request**
> V1alpha1CertificateSigningRequestList list_certificate_signing_request(pretty=pretty, field_selector=field_selector, label_selector=label_selector, resource_version=resource_version, timeout_seconds=timeout_seconds, watch=watch)



list or watch objects of kind CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)
field_selector = 'field_selector_example' # str | A selector to restrict the list of returned objects by their fields. Defaults to everything. (optional)
label_selector = 'label_selector_example' # str | A selector to restrict the list of returned objects by their labels. Defaults to everything. (optional)
resource_version = 'resource_version_example' # str | When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. (optional)
timeout_seconds = 56 # int | Timeout for the list/watch call. (optional)
watch = true # bool | Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. (optional)

try: 
    api_response = api_instance.list_certificate_signing_request(pretty=pretty, field_selector=field_selector, label_selector=label_selector, resource_version=resource_version, timeout_seconds=timeout_seconds, watch=watch)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->list_certificate_signing_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **field_selector** | **str**| A selector to restrict the list of returned objects by their fields. Defaults to everything. | [optional] 
 **label_selector** | **str**| A selector to restrict the list of returned objects by their labels. Defaults to everything. | [optional] 
 **resource_version** | **str**| When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. | [optional] 
 **timeout_seconds** | **int**| Timeout for the list/watch call. | [optional] 
 **watch** | **bool**| Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion. | [optional] 

### Return type

[**V1alpha1CertificateSigningRequestList**](V1alpha1CertificateSigningRequestList.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf, application/json;stream=watch, application/vnd.kubernetes.protobuf;stream=watch

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_certificate_signing_request**
> V1alpha1CertificateSigningRequest patch_certificate_signing_request(name, body, pretty=pretty)



partially update the specified CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
name = 'name_example' # str | name of the CertificateSigningRequest
body = openshift.client.UnversionedPatch() # UnversionedPatch | 
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)

try: 
    api_response = api_instance.patch_certificate_signing_request(name, body, pretty=pretty)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->patch_certificate_signing_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| name of the CertificateSigningRequest | 
 **body** | [**UnversionedPatch**](UnversionedPatch.md)|  | 
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 

### Return type

[**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/merge-patch+json, application/strategic-merge-patch+json
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **read_certificate_signing_request**
> V1alpha1CertificateSigningRequest read_certificate_signing_request(name, pretty=pretty, exact=exact, export=export)



read the specified CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
name = 'name_example' # str | name of the CertificateSigningRequest
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)
exact = true # bool | Should the export be exact.  Exact export maintains cluster-specific fields like 'Namespace' (optional)
export = true # bool | Should this value be exported.  Export strips fields that a user can not specify. (optional)

try: 
    api_response = api_instance.read_certificate_signing_request(name, pretty=pretty, exact=exact, export=export)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->read_certificate_signing_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| name of the CertificateSigningRequest | 
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 
 **exact** | **bool**| Should the export be exact.  Exact export maintains cluster-specific fields like &#39;Namespace&#39; | [optional] 
 **export** | **bool**| Should this value be exported.  Export strips fields that a user can not specify. | [optional] 

### Return type

[**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replace_certificate_signing_request**
> V1alpha1CertificateSigningRequest replace_certificate_signing_request(name, body, pretty=pretty)



replace the specified CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
name = 'name_example' # str | name of the CertificateSigningRequest
body = openshift.client.V1alpha1CertificateSigningRequest() # V1alpha1CertificateSigningRequest | 
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)

try: 
    api_response = api_instance.replace_certificate_signing_request(name, body, pretty=pretty)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->replace_certificate_signing_request: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**| name of the CertificateSigningRequest | 
 **body** | [**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)|  | 
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 

### Return type

[**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replace_certificate_signing_request_approval**
> V1alpha1CertificateSigningRequest replace_certificate_signing_request_approval(body, name, pretty=pretty)



replace approval of the specified CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
body = openshift.client.V1alpha1CertificateSigningRequest() # V1alpha1CertificateSigningRequest | 
name = 'name_example' # str | name of the CertificateSigningRequest
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)

try: 
    api_response = api_instance.replace_certificate_signing_request_approval(body, name, pretty=pretty)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->replace_certificate_signing_request_approval: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)|  | 
 **name** | **str**| name of the CertificateSigningRequest | 
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 

### Return type

[**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **replace_certificate_signing_request_status**
> V1alpha1CertificateSigningRequest replace_certificate_signing_request_status(body, name, pretty=pretty)



replace status of the specified CertificateSigningRequest

### Example 
```python
from __future__ import print_statement
import time
import openshift.client
from kubernetes.client.rest import ApiException
from pprint import pprint

# create an instance of the API class
api_instance = openshift.client.CertificatesV1alpha1Api()
body = openshift.client.V1alpha1CertificateSigningRequest() # V1alpha1CertificateSigningRequest | 
name = 'name_example' # str | name of the CertificateSigningRequest
pretty = 'pretty_example' # str | If 'true', then the output is pretty printed. (optional)

try: 
    api_response = api_instance.replace_certificate_signing_request_status(body, name, pretty=pretty)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling CertificatesV1alpha1Api->replace_certificate_signing_request_status: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)|  | 
 **name** | **str**| name of the CertificateSigningRequest | 
 **pretty** | **str**| If &#39;true&#39;, then the output is pretty printed. | [optional] 

### Return type

[**V1alpha1CertificateSigningRequest**](V1alpha1CertificateSigningRequest.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: */*
 - **Accept**: application/json, application/yaml, application/vnd.kubernetes.protobuf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

