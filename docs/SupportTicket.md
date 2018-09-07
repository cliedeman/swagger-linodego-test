# SupportTicket

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | The ID of the Support Ticket.  | [optional] [default to null]
**Attachments** | **[]string** | A list of filenames representing attached files associated with this Ticket.  | [optional] [default to null]
**Closed** | [**time.Time**](time.Time.md) | The date and time this Ticket was closed.  | [optional] [default to null]
**Description** | **string** | The full details of the issue or question.  | [optional] [default to null]
**Entity** | [***SupportTicketEntity**](SupportTicket_entity.md) |  | [optional] [default to null]
**GravatarId** | **string** | The Gravatar ID of the User who opened this Ticket.  | [optional] [default to null]
**Opened** | [**time.Time**](time.Time.md) | The date and time this Ticket was created.  | [optional] [default to null]
**OpenedBy** | **string** | The User who opened this Ticket.  | [optional] [default to null]
**Status** | **string** | The current status of this Ticket. | [optional] [default to null]
**Summary** | **string** | The summary or title for this Ticket.  | [optional] [default to null]
**Updated** | [**time.Time**](time.Time.md) | The date and time this Ticket was last updated.  | [optional] [default to null]
**UpdatedBy** | **string** | The User who last updated this Ticket.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

