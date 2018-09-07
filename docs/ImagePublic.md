# ImagePublic

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The unique ID of this Image. | [optional] [default to null]
**Label** | **string** | A short description of the Image.  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | When this Image was created. | [optional] [default to null]
**CreatedBy** | **string** | The name of the User who created this Image, or \&quot;linode\&quot; for official Images.  | [optional] [default to null]
**Deprecated** | **bool** | Whether or not this Image is deprecated. Will only be true for deprecated public Images.  | [optional] [default to null]
**Description** | **string** | A detailed description of this Image. | [optional] [default to null]
**IsPublic** | **bool** | True if the Image is public. | [optional] [default to null]
**Size** | **int32** | The minimum size this Image needs to deploy. Size is in MB.  | [optional] [default to null]
**Type_** | **string** | How the Image was created. Manual Images can be created at any time. \&quot;Automatic\&quot; Images are created automatically from a deleted Linode.  | [optional] [default to null]
**Expiry** | [**time.Time**](time.Time.md) | Only Images created automatically (from a deleted Linode; type&#x3D;automatic) will expire.  | [optional] [default to null]
**Vendor** | **string** | The upstream distribution vendor. &#x60;None&#x60; for private Images.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

