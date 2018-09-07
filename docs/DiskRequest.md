# DiskRequest

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Size** | **int32** |  | [default to null]
**Label** | [***Diskpropertieslabel**](Disk/properties/label.md) |  | [default to null]
**Filesystem** | [***Diskpropertiesfilesystem**](Disk/properties/filesystem.md) |  | [optional] [default to null]
**ReadOnly** | **bool** | If true, this Disk is read-only.  | [optional] [default to null]
**Image** | **string** | An Image ID to deploy the Disk from. Official Linode Images start with &#x60;linode/ &#x60;, while your Images start with &#x60;private/&#x60;. See [/images](/#operation/getImages) for more information on the Images available for you to use.  | [optional] [default to null]
**AuthorizedKeys** | **[]string** | A list of public SSH keys that will be automatically appended to the root user&#x27;s &#x60;~/.ssh/authorized_keys&#x60; file.  | [optional] [default to null]
**AuthorizedUsers** | **[]string** | A list of usernames that will have their SSH keys, if any, automatically appended to the root user&#x27;s &#x60;~/.ssh/authorized_keys&#x60; file.  | [optional] [default to null]
**RootPass** | **string** | This will set the root user&#x27;s password on the newly-created Linode. The root password must conform to the following constraints:    * May only use alphanumerics, punctuation, spaces, and tabs.   * Must contain at least two of the following characters classes:     * Upper-case letters     * Lower-case letters     * Digits     * Punctuation  | [optional] [default to null]
**StackscriptId** | **int32** | A StackScript ID that will cause the referenced StackScript to be run during deployment of this Linode. A compatible &#x60;image&#x60; is required to use a StackScript. To get a list of available StackScript and their permitted Images see [/stackscripts](/#operation/getStackScripts). This field cannot be used when deploying from a Backup or a private Image.  | [optional] [default to null]
**StackscriptData** | [***interface{}**](interface{}.md) | This field is required only if the StackScript being deployed requires input data from the User for successful completion. See [Variables and UDFs](https://www.linode.com/docs/platform/stackscripts/#variables-and-udfs) for more details. This field is required to be valid JSON.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

