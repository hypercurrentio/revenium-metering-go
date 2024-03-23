# MeteringRequestDto

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Api** | **string** |  | [optional] [default to null]
**ProductKey** | **string** | The Product Key ID | [optional] [default to null]
**Application** | **string** | The Application ID | [optional] [default to null]
**Method** | **string** | The HTTP method being invoked | [default to null]
**Url** | **string** | The HTTP URL being invoked | [optional] [default to null]
**Metadata** | **string** | Additional billing metadata (supports numeric values and comma-seperated key-value pairs) | [optional] [default to null]
**BackendLatency** | **float64** | Backend API response time | [optional] [default to null]
**GatewayLatency** | **float64** | Latency introduced by the API GW | [optional] [default to null]
**ResponseCode** | **int32** | Backend HTTP response code | [default to null]
**TimedOut** | **bool** | Whether or not the backend timed out | [optional] [default to null]
**RequestMessageSize** | **int64** | The size of the API request in bytes | [optional] [default to null]
**ResponseMessageSize** | **int64** | The size of the API response in bytes | [optional] [default to null]
**RequestHeaders** | **[]string** | The comma seperated list of names of the headers in the request | [default to null]
**ResponseHeaders** | **[]string** | The comma seperated list of names of the headers in the response | [default to null]
**UserAgent** | **string** | The HTTP User Agent | [optional] [default to null]
**RemoteUser** | **string** | The Remote User | [optional] [default to null]
**RemoteHost** | **string** | The Remote Host | [optional] [default to null]
**HttpProtocol** | **string** | The HTTP Protocol | [optional] [default to null]
**ContentType** | **string** | The Content Type | [optional] [default to null]
**CorrelationId** | **string** | The Correlation ID | [optional] [default to null]
**PlatformAPIKey** | **string** | platformAPIKey | [default to null]
**Elements** | [**[]ElementDto**](ElementDTO.md) | Dynamic metering elements | [default to null]
**Source** | **string** | the source of the event | [optional] [default to null]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

