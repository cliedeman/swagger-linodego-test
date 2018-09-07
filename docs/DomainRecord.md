# DomainRecord

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **int32** | This Record&#x27;s unique ID. | [optional] [default to null]
**Type_** | **string** | The type of Record this is in the DNS system. For example, A records associate a domain name with an IPv4 address, and AAAA records associate a domain name with an IPv6 address.  | [optional] [default to null]
**Name** | **string** | The name of this Record. This field&#x27;s actual usage depends on the type of record this represents. For A and AAAA records, this is the subdomain being associated with an IP address.  | [optional] [default to null]
**Target** | **string** | The target for this Record. This field&#x27;s actual usage depends on the type of record this represents. For A and AAAA records, this is the address the named Domain should resolve to.  | [optional] [default to null]
**Priority** | **int32** | The priority of the target host. Lower values are preferred.  | [optional] [default to null]
**Weight** | **int32** | The relative weight of this Record. Higher values are preferred.  | [optional] [default to null]
**Port** | **int32** | The port this Record points to.  | [optional] [default to null]
**Service** | **string** | The service this Record identified. Only valid for SRV records.  | [optional] [default to null]
**Protocol** | **string** | The protocol this Record&#x27;s service communicates with. Only valid for SRV records.  | [optional] [default to null]
**TtlSec** | **int32** | \&quot;Time to Live\&quot; - the amount of time in seconds that this Domain&#x27;s records may be cached by resolvers or other domain servers. Valid values are 300, 3600, 7200, 14400, 28800, 57600, 86400, 172800, 345600, 604800, 1209600, and 2419200 - any other value will be rounded to the nearest valid value.  | [optional] [default to null]
**Tag** | **string** | The tag portion of a CAA record. It is invalid to set this on other record types.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

