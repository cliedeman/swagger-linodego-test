# Body19

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Scopes** | **string** | The scopes to create the token with.  These cannot be changed after creation, and may not exceed the scopes of the acting token. If omitted, the new token will have the same scopes as the acting token.  | [optional] [default to null]
**Expiry** | [**time.Time**](time.Time.md) | When this token should be valid until.  If omitted, the new token will be valid until it is manually revoked.  | [optional] [default to null]
**Label** | [***PersonalAccessTokenpropertieslabel**](PersonalAccessToken/properties/label.md) |  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

