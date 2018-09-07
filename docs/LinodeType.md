# LinodeType

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | The ID representing the Linode Type. | [optional] [default to null]
**Label** | **string** | The Linode Type&#x27;s label is for display purposes only.  | [optional] [default to null]
**Disk** | **int32** | The Disk size, in MB, of the Linode Type.  | [optional] [default to null]
**Class** | **string** | The class of the Linode Type. We currently offer three classes of Linodes:    * nanode - Our entry-level Linode Type.   * standard - Our flagship Linode Type.   * highmem - A Linode Type featuring high memory availability.  | [optional] [default to null]
**Price** | [***LinodeTypePrice**](LinodeType_price.md) |  | [optional] [default to null]
**Addons** | [***LinodeTypeAddons**](LinodeType_addons.md) |  | [optional] [default to null]
**NetworkOut** | **int32** | The Mbits outbound bandwidth allocation.  | [optional] [default to null]
**Memory** | **int32** | Amount of RAM included in this Linode Type.  | [optional] [default to null]
**Transfer** | **int32** | The monthly outbound transfer amount, in MB.  | [optional] [default to null]
**Vcpus** | **int32** | The number of VCPU cores this Linode Type offers.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

