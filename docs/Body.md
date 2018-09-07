# Body

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Username** | **string** | The new User&#x27;s username. This is used for logging in, and may also be displayed alongside actions the User performs (for example, in Events or public StackScripts).  | [default to null]
**Email** | **string** | The new User&#x27;s email address.  | [default to null]
**Restricted** | **bool** | If true, the new User must be granted access to perform actions or access entities on this Account. See [/account/users/{username}/grants](/#operation/getUserGrants) for details on how to configure grants for a restricted User.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

