# {{classname}}

All URIs are relative to *https://api.linode.com/v4*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateClient**](AccountApi.md#CreateClient) | **Post** /account/oauth-clients | Create OAuth Client
[**CreateCreditCard**](AccountApi.md#CreateCreditCard) | **Post** /account/credit-card | Add/Edit Credit Card
[**CreatePayPalPayment**](AccountApi.md#CreatePayPalPayment) | **Post** /account/payments/paypal | Stage PayPal Payment
[**CreatePayment**](AccountApi.md#CreatePayment) | **Post** /account/payments | Make Payment
[**CreateUser**](AccountApi.md#CreateUser) | **Post** /account/users | Create User
[**DeleteClient**](AccountApi.md#DeleteClient) | **Delete** /account/oauth-clients/{clientId} | Delete OAuth Client
[**DeleteUser**](AccountApi.md#DeleteUser) | **Delete** /account/users/{username} | Delete User
[**EventRead**](AccountApi.md#EventRead) | **Post** /account/events/{eventId}/read | Mark Event as Read
[**EventSeen**](AccountApi.md#EventSeen) | **Post** /account/events/{eventId}/seen | Mark Event as Seen
[**ExecutePayPalPayment**](AccountApi.md#ExecutePayPalPayment) | **Post** /account/payment/paypal/execute | Execute Staged/Approved PayPal Payment
[**GetAccount**](AccountApi.md#GetAccount) | **Get** /account | View Account
[**GetAccountSettings**](AccountApi.md#GetAccountSettings) | **Get** /account/settings | View Account Settings
[**GetClient**](AccountApi.md#GetClient) | **Get** /account/oauth-clients/{clientId} | View OAuth Client
[**GetClientThumbnail**](AccountApi.md#GetClientThumbnail) | **Get** /account/oauth-clients/{clientId}/thumbnail | View OAuth Client Thumbnail
[**GetClients**](AccountApi.md#GetClients) | **Get** /account/oauth-clients | List OAuth Clients
[**GetEvent**](AccountApi.md#GetEvent) | **Get** /account/events/{eventId} | View Event
[**GetEvents**](AccountApi.md#GetEvents) | **Get** /account/events | List Events
[**GetInvoice**](AccountApi.md#GetInvoice) | **Get** /account/invoices/{invoiceId} | View Invoice
[**GetInvoiceItems**](AccountApi.md#GetInvoiceItems) | **Get** /account/invoices/{invoiceId}/items | List Invoice Items
[**GetInvoices**](AccountApi.md#GetInvoices) | **Get** /account/invoices | List Invoices
[**GetNotifications**](AccountApi.md#GetNotifications) | **Get** /account/notifications | List Notifications
[**GetPayment**](AccountApi.md#GetPayment) | **Get** /account/payments/{paymentId} | View Payment
[**GetPayments**](AccountApi.md#GetPayments) | **Get** /account/payments | List Payments
[**GetTransfer**](AccountApi.md#GetTransfer) | **Get** /account/transfer | View Network Utilization
[**GetUser**](AccountApi.md#GetUser) | **Get** /account/users/{username} | View User
[**GetUserGrants**](AccountApi.md#GetUserGrants) | **Get** /account/users/{username}/grants | View User&#x27;s grants
[**GetUsers**](AccountApi.md#GetUsers) | **Get** /account/users | List Users
[**ResetClientSecret**](AccountApi.md#ResetClientSecret) | **Post** /account/oauth-clients/{clientId}/reset-secret | Reset OAuth Client Secret
[**SetClientThumbnail**](AccountApi.md#SetClientThumbnail) | **Put** /account/oauth-clients/{clientId}/thumbnail | Update OAuth Client Thumbnail
[**UpdateAccount**](AccountApi.md#UpdateAccount) | **Put** /account | Update Account
[**UpdateAccountSettings**](AccountApi.md#UpdateAccountSettings) | **Put** /account/settings | Update Account Settings
[**UpdateClient**](AccountApi.md#UpdateClient) | **Put** /account/oauth-clients/{clientId} | Update OAuth Client
[**UpdateUser**](AccountApi.md#UpdateUser) | **Put** /account/users/{username} | Update User
[**UpdateUserGrants**](AccountApi.md#UpdateUserGrants) | **Put** /account/users/{username}/grants | Update User&#x27;s grants

# **CreateClient**
> OAuthClient CreateClient(ctx, )
Create OAuth Client

Creates an OAuth Client, which can be used to allow users (using their Linode account) to log in to your own application, and optionally grant your application some amount of access to their Linodes or other entities. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.

### Return type

[**OAuthClient**](OAuthClient.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateCreditCard**
> interface{} CreateCreditCard(ctx, body)
Add/Edit Credit Card

Adds/edit credit card information to your Account. Only one credit card can be associated with your Account, so using this endpoint will overwrite your currently active card information with the new credit card. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**CreditCard**](CreditCard.md)| Update the credit card information associated with your Account. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreatePayPalPayment**
> InlineResponse2006 CreatePayPalPayment(ctx, body)
Stage PayPal Payment

This begins the process of submitting a Payment via PayPal. After calling this endpoint, you must take the resulting `payment_id` along with the `payer_id` from your PayPal account and [POST /account/payments/paypal-execute](/#operation/executePayPalPayment) to complete the Payment. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**PayPal**](PayPal.md)| The amount of the Payment to submit via PayPal.
 | 

### Return type

[**InlineResponse2006**](inline_response_200_6.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreatePayment**
> Payment CreatePayment(ctx, body)
Make Payment

Makes a Payment to your Account via credit card. This will charge your credit card the requested amount. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**PaymentRequest**](PaymentRequest.md)| Information about the Payment you are making. | 

### Return type

[**Payment**](Payment.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **CreateUser**
> User CreateUser(ctx, )
Create User

Creates a User on your Account. Once created, the User will be able to log in and access portions of your Account. Access is determined by whether or not they are restricted, and what grants they have been given. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.

### Return type

[**User**](User.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteClient**
> interface{} DeleteClient(ctx, clientId)
Delete OAuth Client

Deletes an OAuth Client registered with Linode. The Client ID and Client secret will no longer be accepted by https://login.linode.com, and all tokens issued to this client will be invalidated (meaning that if your application was using a token, it will no longer work). 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **clientId** | **string**| The OAuth Client ID to look up. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **DeleteUser**
> interface{} DeleteUser(ctx, username)
Delete User

Deletes a User. The deleted User will be immediately logged out and may no longer log in or perform any actions. All of the User's Grants will be removed. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| The username to look up. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **EventRead**
> interface{} EventRead(ctx, eventId)
Mark Event as Read

Marks a single Event as read.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **eventId** | **int32**| The ID of the Event to designate as read. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **EventSeen**
> interface{} EventSeen(ctx, eventId)
Mark Event as Seen

Marks all Events up to and including this Event by ID as seen. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **eventId** | **int32**| The ID of the Event to designate as seen. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ExecutePayPalPayment**
> interface{} ExecutePayPalPayment(ctx, body)
Execute Staged/Approved PayPal Payment

Given a PaymentID and PayerID - as generated by PayPal during the transaction authorization process - this endpoint executes the Payment to capture the funds and credit your Linode Account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**PayPalExecute**](PayPalExecute.md)| The details of the Payment to execute.
 | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetAccount**
> Account GetAccount(ctx, )
View Account

Returns the contact and billing information related to your Account. 

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**Account**](Account.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetAccountSettings**
> AccountSettings GetAccountSettings(ctx, )
View Account Settings

Returns information related to your Account settings: Managed service subscription, Longview subscription, and network helper. 

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**AccountSettings**](AccountSettings.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetClient**
> OAuthClient GetClient(ctx, clientId)
View OAuth Client

Returns information about a single OAuth client. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **clientId** | **string**| The OAuth Client ID to look up. | 

### Return type

[**OAuthClient**](OAuthClient.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetClientThumbnail**
> string GetClientThumbnail(ctx, clientId)
View OAuth Client Thumbnail

Returns the thumbnail for this OAuth Client.  This is a publicly-viewable endpoint, and can be accessed without authentication. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **clientId** | **string**| The OAuth Client ID to look up. | 

### Return type

**string**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: image/png, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetClients**
> InlineResponse2004 GetClients(ctx, optional)
List OAuth Clients

Returns a paginated list of OAuth Clients registered to your Account.  OAuth Clients allow users to log into applications you write or host using their Linode Account, and may allow them to grant some level of access to their Linodes or other entities to your application. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetClientsOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetClientsOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**InlineResponse2004**](inline_response_200_4.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetEvent**
> Event GetEvent(ctx, eventId)
View Event

Returns a single Event object.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **eventId** | **int32**| The ID of the Event. | 

### Return type

[**Event**](Event.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetEvents**
> InlineResponse200 GetEvents(ctx, optional)
List Events

Returns a collection of Event objects representing actions taken on your Account. The Events returned depends on your grants. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetEventsOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetEventsOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**InlineResponse200**](inline_response_200.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetInvoice**
> Invoice GetInvoice(ctx, invoiceId)
View Invoice

Returns a single Invoice object.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **invoiceId** | **int32**| The ID of the Invoice. | 

### Return type

[**Invoice**](Invoice.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetInvoiceItems**
> InlineResponse2002 GetInvoiceItems(ctx, invoiceId, optional)
List Invoice Items

Returns a paginated list of Invoice items.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **invoiceId** | **int32**| The ID of the Invoice. | 
 **optional** | ***GetInvoiceItemsOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetInvoiceItemsOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**InlineResponse2002**](inline_response_200_2.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetInvoices**
> InlineResponse2001 GetInvoices(ctx, optional)
List Invoices

Returns a paginated list of Invoices against your Account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetInvoicesOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetInvoicesOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**InlineResponse2001**](inline_response_200_1.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetNotifications**
> InlineResponse2003 GetNotifications(ctx, )
List Notifications

Returns a collection of Notification objects representing important, often time-sensitive items related to your Account. You cannot interact directly with Notifications, and a Notification will disappear when the circumstances causing it have been resolved. For example, if you have an important Ticket open, you must respond to the Ticket to dismiss the Notification. 

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**InlineResponse2003**](inline_response_200_3.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetPayment**
> Payment GetPayment(ctx, paymentId)
View Payment

Returns information about a specific Payment. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **paymentId** | **int32**| The ID of the Payment to look up. | 

### Return type

[**Payment**](Payment.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetPayments**
> InlineResponse2005 GetPayments(ctx, optional)
List Payments

Returns a paginated list of Payments made on this Account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetPaymentsOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetPaymentsOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**InlineResponse2005**](inline_response_200_5.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetTransfer**
> Transfer GetTransfer(ctx, )
View Network Utilization

Returns a Transfer object showing your network utilization, in GB, for the current month. 

### Required Parameters
This endpoint does not need any parameter.

### Return type

[**Transfer**](Transfer.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetUser**
> User GetUser(ctx, username)
View User

Returns information about a single User on your Account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| The username to look up. | 

### Return type

[**User**](User.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetUserGrants**
> GrantsResponse GetUserGrants(ctx, username)
View User's grants

Returns the full grants structure for this User. This includes all entities on the Account alongside what level of access this User has to each of them. Individual users may view their own grants at the [/profile/grants](/#operation/getProfileGrants) endpoint, but will not see entities that they have no access to. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| The username to look up. | 

### Return type

[**GrantsResponse**](GrantsResponse.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetUsers**
> InlineResponse2007 GetUsers(ctx, optional)
List Users

Returns a paginated list of Users on your Account. Users may access all or part of your Account based on their restricted status and grants.  An unrestricted User may access everything on the account, whereas restricted User may only access entities or perform actions they've been given specific grants to. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***GetUsersOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a GetUsersOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **optional.Int32**| The page of a collection to return. | 
 **pageSize** | **optional.Int32**| The number of items to return per page. | 

### Return type

[**InlineResponse2007**](inline_response_200_7.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ResetClientSecret**
> OAuthClient ResetClientSecret(ctx, clientId)
Reset OAuth Client Secret

Resets the OAuth Client secret for a client you own, and returns the OAuth Client with the plaintext secret. This secret is not supposed to be publicly known or disclosed anywhere. This can be used to generate a new secret in case the one you have has been leaked, or to get a new secret if you lost the original. The old secret is expired immediately, and logins to your client with the old secret will fail. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **clientId** | **string**| The OAuth Client ID to look up. | 

### Return type

[**OAuthClient**](OAuthClient.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **SetClientThumbnail**
> interface{} SetClientThumbnail(ctx, body, clientId)
Update OAuth Client Thumbnail

Upload a thumbnail for a client you own.  You must upload an image file that will be returned when the thumbnail is retrieved.  This image will be publicly-viewable. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Object**](Object.md)| The image to set as the thumbnail. | 
  **clientId** | **string**| The OAuth Client ID to look up. | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: image/png
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateAccount**
> Account UpdateAccount(ctx, body)
Update Account

Updates contact and billing information related to your Account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**Account**](Account.md)| Update contact and billing information. | 

### Return type

[**Account**](Account.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateAccountSettings**
> AccountSettings UpdateAccountSettings(ctx, body)
Update Account Settings

Updates your Account settings. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**AccountSettings**](AccountSettings.md)| Update Account settings information. | 

### Return type

[**AccountSettings**](AccountSettings.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateClient**
> OAuthClient UpdateClient(ctx, clientId, )
Update OAuth Client

Update information about an OAuth Client on your Account. This can be especially useful to update the `redirect_uri` of your client in the event that the callback url changed in your application. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **clientId** | **string**| The OAuth Client ID to look up. | 

### Return type

[**OAuthClient**](OAuthClient.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateUser**
> User UpdateUser(ctx, username, )
Update User

Update information about a User on your Account. This can be used to change the restricted status of a User. When making a User restricted, no grants will be configured by default and you must then set up grants in order for the User to access anything on the Account. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **username** | **string**| The username to look up. | 

### Return type

[**User**](User.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateUserGrants**
> GrantsResponse UpdateUserGrants(ctx, body, username)
Update User's grants

Update the grants a User has. This can be used to give a User access to new entities or actions, or take access away.  You do not need to include the grant for every entity on the Account in this request; any that are not included will remain unchanged. 

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**GrantsResponse**](GrantsResponse.md)| The grants to update. Omitted grants will be left unchanged. | 
  **username** | **string**| The username to look up. | 

### Return type

[**GrantsResponse**](GrantsResponse.md)

### Authorization

[oauth](../README.md#oauth), [personalAccessToken](../README.md#personalAccessToken)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

