# AuthorizedApp

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | This authorization&#x27;s ID, used for revoking access.  | [optional] [default to null]
**Label** | **string** | The name of the application you&#x27;ve authorized.  | [optional] [default to null]
**ThumbnailUrl** | **string** | The URL at which this app&#x27;s thumbnail may be accessed.  | [optional] [default to null]
**Scopes** | **string** | The OAuth scopes this app was authorized with.  This defines what parts of your Account the app is allowed to access.  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | When this app was authorized. | [optional] [default to null]
**Expiry** | [**time.Time**](time.Time.md) | When this app&#x27;s access token expires.  Please note that apps may still have active refresh tokens after this time passes.  | [optional] [default to null]
**Website** | **string** | The website where you can get more information about this app.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

