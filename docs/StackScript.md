# StackScript

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | The unique ID of this StackScript. | [optional] [default to null]
**Username** | **string** | The User who created the StackScript.  | [optional] [default to null]
**UserGravatarId** | **string** | The Gravatar ID for the User who created the StackScript.  | [optional] [default to null]
**Label** | **string** | The StackScript&#x27;s label is for display purposes only.  | [optional] [default to null]
**Description** | **string** | A description for the StackScript.  | [optional] [default to null]
**Images** | **[]string** | An array of Image IDs representing the Images that this StackScript is compatible for deploying with.  | [optional] [default to null]
**DeploymentsTotal** | **int32** | The total number of times this StackScript has been deployed.  | [optional] [default to null]
**DeploymentsActive** | **int32** | Count of currently active, deployed Linodes created from this StackScript.  | [optional] [default to null]
**IsPublic** | **bool** | This determines whether other users can use your StackScript. **Once a StackScript is made public, it cannot be made private.**  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | The date this StackScript was created.  | [optional] [default to null]
**Updated** | [**time.Time**](time.Time.md) | The date this StackScript was last updated.  | [optional] [default to null]
**RevNote** | **string** | This field allows you to add notes for the set of revisions made to this StackScript.  | [optional] [default to null]
**Script** | **string** | The script to execute when provisioning a new Linode with this StackScript.  | [optional] [default to null]
**UserDefinedFields** | [**[]UserDefinedField**](UserDefinedField.md) | This is a list of fields defined with a special syntax inside this StackScript that allow for supplying customized parameters during deployment. See [Variables and UDFs](https://www.linode.com/docs/platform/stackscripts/#variables-and-udfs) for more information.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

