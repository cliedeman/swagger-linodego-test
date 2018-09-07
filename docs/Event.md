# Event

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | The unique ID of this Event. | [optional] [default to null]
**Action** | **string** | The action that caused this Event. New actions may be added in the future.  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | When this Event was created. | [optional] [default to null]
**Entity** | [***EventEntity**](Event_entity.md) |  | [optional] [default to null]
**PercentComplete** | **int32** | A percentage estimating the amount of time remaining for an Event. Returns &#x60;null&#x60; for notification events.  | [optional] [default to null]
**Rate** | **string** | The rate of completion of the Event. Only some Events will return rate; for example, migration and resize Events.  | [optional] [default to null]
**Read** | **bool** | If this Event has been read. | [optional] [default to null]
**Seen** | **bool** | If this Event has been seen. | [optional] [default to null]
**Status** | **string** | The current status of this Event. | [optional] [default to null]
**TimeRemaining** | **int32** | The estimated time remaining until the completion of this Event. This value is only returned for in-progress events.  | [optional] [default to null]
**Username** | **string** | The username of the User who caused the Event.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

