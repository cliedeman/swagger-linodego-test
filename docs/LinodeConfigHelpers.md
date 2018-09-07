# LinodeConfigHelpers

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**UpdatedbDisabled** | **bool** | Disables updatedb cron job to avoid disk thrashing. | [optional] [default to null]
**Distro** | **bool** | Helps maintain correct inittab/upstart console device. | [optional] [default to null]
**ModulesDep** | **bool** | Creates a modules dependency file for the Kernel you run. | [optional] [default to null]
**Network** | **bool** | Automatically configures static networking. | [optional] [default to null]
**DevtmpfsAutomount** | **bool** | Populates the /dev directory early during boot without udev.  Defaults to false.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

