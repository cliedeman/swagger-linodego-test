# Body1

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BackupId** | **int32** | A Backup ID from another Linode&#x27;s available backups. Your User must have &#x60;read_write&#x60; access to that Linode, the Backup must have a &#x60;status&#x60; of &#x60;successful&#x60;, and the Linode must be deployed to the same &#x60;region&#x60; as the Backup. See [/linode/instances/{linodeId}/backups](/#operation/getBackups) for a Linode&#x27;s available backups.  This field and the &#x60;image&#x60; field are mutually exclusive.  | [optional] [default to null]
**BackupsEnabled** | **bool** | If this field is set to &#x60;true&#x60;, the created Linode will automatically be enrolled in the Linode Backup service. This will incur an additional charge. The cost for the Backup service is dependent on the Type of Linode deployed.  Backup pricing is included in the response from [/linodes/types](/#operation/getLinodeTypes)  | [optional] [default to null]
**SwapSize** | **int32** | When deploying from an Image, this field is optional, otherwise it is ignored. This is used to set the swap disk size for the newly-created Linode.  | [optional] [default to 512]
**Type_** | **string** | The [Linode Type](#operation/getLinodeTypes) of the Linode you are creating.  | [default to null]
**Region** | **string** | The [Region](#operation/getRegions) where the Linode will be located.  | [default to null]
**Image** | **string** | An Image ID to deploy the Disk from. Official Linode Images start with &#x60;linode/ &#x60;, while your Images start with &#x60;private/&#x60;. See [/images](/#operation/getImages) for more information on the Images available for you to use.  | [optional] [default to null]
**RootPass** | **string** | The password for the root user on the newly-created Linode. Only accepted if \&quot;image\&quot; is provided.  | [optional] [default to null]
**AuthorizedKeys** | **[]string** | A list of SSH public keys to deploy for the root user on the newly-created Linode.  Only accepted if &#x60;image&#x60; is provided.  | [optional] [default to null]
**StackscriptId** | **int32** | The StackScript to deploy to the newly-created Linode.  If provided, \&quot;image\&quot; must also be provided, and must be an Image that is compatible with this StackScript.  | [optional] [default to null]
**StackscriptData** | [***interface{}**](interface{}.md) | An object containing responses to any User Defined Fields present in the StackScript being deployed to this Linode. Only accepted if &#x60;stackscript_id&#x60; is given.  The required values depend on the StackScript being deployed.  | [optional] [default to null]
**Booted** | **bool** | Whether to boot this Linode after the deploy is complete. Defaults to true if &#x60;image&#x60; is provided. Not accepted if not deploying from an Image.  | [optional] [default to null]
**Label** | [***Linodepropertieslabel**](Linode/properties/label.md) |  | [optional] [default to null]
**Group** | [***Linodepropertiesgroup**](Linode/properties/group.md) |  | [optional] [default to null]
**PrivateIp** | **bool** | If true, the created Linode will have private networking enabled.  | [optional] [default to null]
**AuthorizedUsers** | **[]string** | A list of usernames. If the usernames have associated SSH keys, the keys will be appended to the root users &#x60;~/.ssh/authorized_keys&#x60; file automatically.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

