# Volume

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | The unique ID of this Volume. | [optional] [default to null]
**Label** | **string** | The Volume&#x27;s label is for display purposes only.  | [default to null]
**FilesystemPath** | **string** | The full filesystem path for the Volume based on the Volume&#x27;s label. Path is /dev/disk/by-id/scsi-0Linode_Volume_ + Volume label.  | [optional] [default to null]
**Status** | **string** | The current status of the volume.  Can be one of:    * &#x60;creating&#x60; - the Volume is being created and is not yet available     for use.   * &#x60;active&#x60; - the Volume is online and available for use.   * &#x60;resizing&#x60; - the Volume is in the process of upgrading     its current capacity.   * &#x60;contact_support&#x60; - there is a problem with your Volume. Please     [open a Support Ticket](/#operation/createTicket) to resolve the issue.  | [optional] [default to null]
**Size** | **int32** | The Volume&#x27;s size, in GiB.  | [optional] [default to null]
**Region** | [***Regionpropertiesid**](Region/properties/id.md) |  | [optional] [default to null]
**LinodeId** | **int32** | If a Volume is attached to a specific Linode, the ID of that Linode will be displayed here.  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | When this Volume was created. | [optional] [default to null]
**Updated** | [**time.Time**](time.Time.md) | When this Volume was last updated. | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

