# LinodeAlerts

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Cpu** | **int32** | The percentage of CPU usage required to trigger an alert. If the average CPU usage over two hours exceeds this value, we&#x27;ll send you an alert. If this is set to 0, the alert is disabled.  | [optional] [default to null]
**NetworkIn** | **int32** | The amount of incoming traffic, in Mbit/s, required to trigger an alert. If the average incoming traffic over two hours exceeds this value, we&#x27;ll send you an alert. If this is set to 0 (zero), the alert is disabled.  | [optional] [default to null]
**NetworkOut** | **int32** | The amount of outbound traffic, in Mbit/s, required to trigger an alert. If the average outbound traffic over two hours exceeds this value, we&#x27;ll send you an alert. If this is set to 0 (zero), the alert is disabled.  | [optional] [default to null]
**TransferQuota** | **int32** | The percentage of network transfer that may be used before an alert is triggered. When this value is exceeded, we&#x27;ll alert you. If this is set to 0 (zero), the alert is disabled.  | [optional] [default to null]
**Io** | **int32** | The amount of disk IO operation per second required to trigger an alert. If the average disk IO over two hours exceeds this value, we&#x27;ll send you an alert. If set to 0, this alert is disabled.  | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

