# PersonalAccessToken

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | This token&#x27;s unique ID, which can be used to revoke it.  | [optional] [default to null]
**Scopes** | **string** | The scopes this token was created with. These define what parts of the Account the token can be used to access. Many command-line tools, such as the [Linode CLI](https://github.com/linode/linode-cli), require tokens with access to &#x60;*&#x60;. Tokens with more restrictive scopes are generally more secure.  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | The date and time this token was created.  | [optional] [default to null]
**Label** | **string** | This token&#x27;s label.  This is for display purposes only, but can be used to more easily track what you&#x27;re using each token for.  | [optional] [default to null]
**Token** | **string** | The token used to access the API.  When the token is created, the full token is returned here.  Otherwise, only the first 16 characters are returned.  | [optional] [default to null]
**Expiry** | [**time.Time**](time.Time.md) | When this token will expire.  Personal Access Tokens cannot be renewed, so after this time the token will be completely unusable and a new token will need to be generated.  Tokens may be created with \&quot;null\&quot; as their expiry and will never expire unless revoked.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

