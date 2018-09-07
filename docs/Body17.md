# Body17

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Region** | **string** | The ID of the Region to create this NodeBalancer in.  | [default to null]
**Label** | [***NodeBalancerpropertieslabel**](NodeBalancer/properties/label.md) |  | [optional] [default to null]
**ClientConnThrottle** | [***NodeBalancerpropertiesclientConnThrottle**](NodeBalancer/properties/client_conn_throttle.md) |  | [optional] [default to null]
**Configs** | [**[]Object**](.md) | The ports to configure this NodeBalancer with on creation. Each config must have a unique port and at least one Node.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

