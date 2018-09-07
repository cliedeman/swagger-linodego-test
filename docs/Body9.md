# Body9

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | **string** | The IP address.  | [optional] [default to null]
**Gateway** | **string** | The default gateway for this address.  | [optional] [default to null]
**SubnetMask** | **string** | The mask that separates host bits from network bits for this address.  | [optional] [default to null]
**Prefix** | **int32** | The number of bits set in the subnet mask.  | [optional] [default to null]
**Type_** | **string** | The type of address this is.  | [optional] [default to null]
**Public** | **bool** | Whether this is a public or private IP address.  | [optional] [default to null]
**Rdns** | **string** | The reverse DNS assigned to this address. For public IPv4 addresses, this will be set to a default value provided by Linode if not explicitly set.  | [optional] [default to null]
**LinodeId** | **int32** | The ID of the Linode this address currently belongs to. For IPv4 addresses, this is by default the Linode that this address was assigned to on creation, and these addresses my be moved using the [/networking/ipv4/assign](/#operation/assignIPs) endpoint. For SLAAC and link-local addresses, this value may not be changed.  | [optional] [default to null]
**Region** | **string** | The Region this IP address resides in.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

