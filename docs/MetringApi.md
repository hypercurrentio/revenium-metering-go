# {{classname}}

All URIs are relative to *https://api.revenium.io/meter/v1/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Meter**](MetringApi.md#Meter) | **Post** /meter | Insert API metering data
[**Valid**](MetringApi.md#Valid) | **Get** /meter/product-key | Determine if a ProductKey is valid or not

# **Meter**
> Unit Meter(ctx, body)
Insert API metering data

Insert API metering data

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **body** | [**MeteringRequestDto**](MeteringRequestDto.md)|  | 

### Return type

[**Unit**](Unit.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **Valid**
> interface{} Valid(ctx, optional)
Determine if a ProductKey is valid or not

Determine if a ProductKey is valid or not

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***MetringApiValidOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a MetringApiValidOpts struct
Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **productKey** | **optional.String**| The product key | 
 **application** | **optional.String**| The application ID | 

### Return type

[**interface{}**](interface{}.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

