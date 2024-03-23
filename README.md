# Go API client for metering

Revenium Metering API

## Overview
This API client was generated by the [swagger-codegen](https://github.com/swagger-api/swagger-codegen) project.  By using the [swagger-spec](https://github.com/swagger-api/swagger-spec) from a remote server, you can easily generate an API client.

- API version: 1.14.0-SNAPSHOT
- Package version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.go.GoClientCodegen
For more information, please visit [https://revenium.io](https://revenium.io)

## Installation
Put the package under your project folder and add the following in import:
```golang
import "./metering"
```

## Documentation for API Endpoints

All URIs are relative to *https://api.revenium.io/meter/v1/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*EventsApi* | [**SaveEvent**](docs/EventsApi.md#saveevent) | **Post** /event | Save can API event
*MetringApi* | [**Meter**](docs/MetringApi.md#meter) | **Post** /meter | Insert API metering data
*MetringApi* | [**Valid**](docs/MetringApi.md#valid) | **Get** /meter/product-key | Determine if a ProductKey is valid or not

## Documentation For Models

 - [ApiEventDto](docs/ApiEventDto.md)
 - [ElementDto](docs/ElementDto.md)
 - [MeteringRequestDto](docs/MeteringRequestDto.md)
 - [Unit](docs/Unit.md)

## Documentation For Authorization

## x-api-key
- **Type**: API key 

Example
```golang
auth := context.WithValue(context.Background(), sw.ContextAPIKey, sw.APIKey{
	Key: "APIKEY",
	Prefix: "Bearer", // Omit if not necessary.
})
r, err := client.Service.Operation(auth, args)
```

## Author

info@revenium.io