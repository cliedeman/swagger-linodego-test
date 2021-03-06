# {{classname}}

All URIs are relative to *https://api.linode.com/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**AttachVolume**](VolumesApi.md#AttachVolume) | **Post** /volumes/{volumeId}/attach | Attach Volume
[**CloneVolume**](VolumesApi.md#CloneVolume) | **Post** /volumes/{volumeId}/clone | Clone Volume
[**CreateVolume**](VolumesApi.md#CreateVolume) | **Post** /volumes | Create Volume
[**DeleteVolume**](VolumesApi.md#DeleteVolume) | **Delete** /volumes/{volumeId} | Delete Volume
[**DetachVolume**](VolumesApi.md#DetachVolume) | **Post** /volumes/{volumeId}/detach | Detach Volume
[**GetVolume**](VolumesApi.md#GetVolume) | **Get** /volumes/{volumeId} | View Volume
[**GetVolumes**](VolumesApi.md#GetVolumes) | **Get** /volumes | List Volumes
[**ResizeVolume**](VolumesApi.md#ResizeVolume) | **Post** /volumes/{volumeId}/resize | Resize Volume
[**UpdateVolume**](VolumesApi.md#UpdateVolume) | **Put** /volumes/{volumeId} | Update Volume

# **AttachVolume**
> Volume AttachVolume(ctx, body, volumeId)
Attach Volume

Attaches a Volume on your Account to an existing Linode on your Account. In order for this request to complete successfully, your User must have `read_only` or `read_write` permission to the Volume and `read_write` permission to the Linode. Additionally, the Volume and Linode must be located in the same Region. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Body23**](Body23.md)| Volume to attach to a Linode. | 
  **volumeId** | **int32**| ID of the Volume to attach. | 

### Return type

[**Volume**](Volume.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CloneVolume**
> interface{} CloneVolume(ctx, body, volumeId)
Clone Volume

Creates a Volume on your Account. In order for this request to complete successfully, your User must have the `add_volumes` grant. The new Volume will have the same size and data as the source Volume. Creating a new Volume will incur a charge on your Account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Body24**](Body24.md)| The requested state your Volume will be cloned into. | 
  **volumeId** | **int32**| ID of the Volume to clone. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateVolume**
> Volume CreateVolume(ctx, body)
Create Volume

Creates a Volume on your Account. In order for this to complete successfully, your User must have the `add_volumes` grant. Creating a new Volume will start accruing additional charges on your account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Body22**](Body22.md)| The requested initial state of a new Volume. | 

### Return type

[**Volume**](Volume.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteVolume**
> interface{} DeleteVolume(ctx, volumeId)
Delete Volume

Deletes a Volume you have permission to `read_write`.  **Deleting a Volume is a destructive action and cannot be undone.**  Deleting stops billing for the Volume. You will be billed for time used within the billing period the Volume was active. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **volumeId** | **int32**| ID of the Volume to look up. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DetachVolume**
> interface{} DetachVolume(ctx, volumeId)
Detach Volume

Detaches a Volume on your Account from a Linode on your Account. In order for this request to complete successfully, your User must have `read_write` access to the Volume and `read_write` access to the Linode. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **volumeId** | **int32**| ID of the Volume to detach. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetVolume**
> Volume GetVolume(ctx, volumeId, optional)
View Volume

Get information about a single Volume. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **volumeId** | **int32**| ID of the Volume to look up. | 
 **optional** | ***GetVolumeOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetVolumeOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**Volume**](Volume.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetVolumes**
> InlineResponse20016 GetVolumes(ctx, optional)
List Volumes

Returns a paginated list of Volumes you have permission to view. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetVolumesOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetVolumesOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**InlineResponse20016**](inline_response_200_16.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ResizeVolume**
> interface{} ResizeVolume(ctx, body, volumeId)
Resize Volume

Resize an existing Volume on your Account. In order for this request to complete successfully, your User must have the `read_write` permissions to the Volume. * Volumes can only be resized up. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Body25**](Body25.md)| The requested size to increase your Volume to. | 
  **volumeId** | **int32**| ID of the Volume to resize. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateVolume**
> Volume UpdateVolume(ctx, body, volumeId)
Update Volume

Updates a Volume that you have permission to `read_write`. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Object**](.md)| If any updated field fails to pass validation, the Volume will not be updated.
 | 
  **volumeId** | **int32**| ID of the Volume to look up. | 

### Return type

[**Volume**](Volume.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

