# LinodeConfig

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | The ID of this Config. | [optional] [default to null]
**Kernel** | **string** | A Kernel ID to boot a Linode with. Defaults to \&quot;linode/latest-64bit\&quot;. | [optional] [default to null]
**Comments** | **string** | Optional field for arbitrary User comments on this Config. | [optional] [default to null]
**MemoryLimit** | **int32** | Defaults to the total RAM of the Linode.  | [optional] [default to null]
**RunLevel** | **string** | Defines the state of your Linode after booting. Defaults to &#x60;default&#x60;.  | [optional] [default to null]
**VirtMode** | **string** | Controls the virtualization mode. Defaults to &#x60;paravirt&#x60;. * &#x60;paravirt&#x60; is suitable for most cases. Linodes running in paravirt mode   share some qualities with the host, ultimately making it run faster since   there is less transition between it and the host. * &#x60;full_virt&#x60; affords more customization, but is slower because 100% of the VM   is virtualized.  | [optional] [default to null]
**Helpers** | [***LinodeConfigHelpers**](LinodeConfig_helpers.md) |  | [optional] [default to null]
**Label** | **string** | The Config&#x27;s label is for display purposes only.  | [default to null]
**Devices** | [***Devices**](Devices.md) |  | [default to null]
**RootDevice** | **string** | The root device to boot. The corresponding disk must be attached.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

