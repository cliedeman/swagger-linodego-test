# Backup

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | The unique ID of this Backup. | [optional] [default to null]
**Type_** | **string** | This indicates whether the Backup is an automatic Backup or manual snapshot taken by the User at a specific point in time.  | [optional] [default to null]
**Status** | **string** | The current state of a specific Backup. | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | The date the Backup was taken. | [optional] [default to null]
**Updated** | [**time.Time**](time.Time.md) | The date the Backup was most recently updated. | [optional] [default to null]
**Finished** | [**time.Time**](time.Time.md) | The date the Backup completed. | [optional] [default to null]
**Label** | **string** | A label for Backups that are of type &#x60;snapshot&#x60;. | [optional] [default to null]
**Configs** | **[]string** | A list of the labels of the Configuration profiles that are part of the Backup.  | [optional] [default to null]
**Disks** | [**[]BackupDisks**](Backup_disks.md) | A list of the disks that are part of the Backup.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

