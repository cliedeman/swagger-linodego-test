# NodeBalancer

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | This NodeBalancer&#x27;s unique ID.  | [optional] [default to null]
**Label** | **string** | This NodeBalancer&#x27;s label. These must be unique on your Account.  | [optional] [default to null]
**Region** | **string** | The Region where this NodeBalancer is located. NodeBalancers only support backends in the same Region.  | [optional] [default to null]
**Hostname** | **string** | This NodeBalancer&#x27;s hostname, ending with _.nodebalancer.linode.com_  | [optional] [default to null]
**Ipv4** | **string** | This NodeBalancer&#x27;s public IPv4 address.  | [optional] [default to null]
**Ipv6** | **string** | This NodeBalancer&#x27;s public IPv6 address.  | [optional] [default to null]
**Created** | [**time.Time**](time.Time.md) | When this NodeBalancer was created.  | [optional] [default to null]
**Updated** | [**time.Time**](time.Time.md) | When this NodeBalancer was last updated.  | [optional] [default to null]
**ClientConnThrottle** | **int32** | Throttle connections per second.  Set to 0 (zero) to disable throttling.  | [optional] [default to null]
**Transfer** | [***NodeBalancerTransfer**](NodeBalancer_transfer.md) |  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

