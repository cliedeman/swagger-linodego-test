# ManagedService

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | This Service&#x27;s unique ID.  | [optional] [default to null]
**Status** | **string** | The current status of this Service.  | [optional] [default to null]
**ServiceType** | **string** | How this Service is monitored.  | [optional] [default to null]
**Label** | **string** | The label for this Service. This is for display purposes only.  | [optional] [default to null]
**Address** | **string** | The URL at which this Service is monitored.  | [optional] [default to null]
**Timeout** | **int32** | How long to wait, in seconds, for a response before considering the Service to be down.  | [optional] [default to null]
**Body** | **string** | What to expect to find in the response body for the Service to be considered up.  | [optional] [default to null]
**ConsultationGroup** | **string** | The group of ManagedContacts who should be notified or consulted with when an Issue is detected.  | [optional] [default to null]
**Notes** | **string** | Any information relevant to the Service that Linode special forces should know when attempting to resolve Issues.  | [optional] [default to null]
**Region** | **string** | The Region in which this Service is located. This is required if address is a private IP, and may not be set otherwise.  | [optional] [default to null]
**Credentials** | **[]int32** | An array of ManagedCredential IDs that should be used when attempting to resolve issues with this Service.  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | When this Managed Service was created. | [optional] [default to null]
**Updated** | [**time.Time**](time.Time.md) | When this Managed Service was last updated. | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

