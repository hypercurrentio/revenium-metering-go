# Revenium Metering SDK for Go

## Overview

Go SDK for Revenium Metering API. This SDK allows you to dispatch metering metadata for API calls to Revenium.

For more information, please visit [https://revenium.io](https://revenium.io)

## Installation
```shell
go get -u github.com/hypercurrentio/revenium-metering-go@v1.0.0
```

## Example

```golang
package main

import (
	"context"
	metering "github.com/hypercurrentio/revenium-metering-go"
	"os"
)

func main() {
	cfg := metering.NewConfiguration()
	cfg.BasePath = "https://api.revenium.io/meter/v1/api"
	cfg.DefaultHeader["x-api-key"] = os.Getenv("REVENIUM_API_KEY")

	apiClient := metering.NewAPIClient(cfg)

	request := metering.MeteringRequestDto{
		Method:          "GET",
		Url:             "https://api.weyland-yutani.io/request",
		Application:     "d9680f8e-1ec2-4f24-892d-99b779224604",
		ResponseCode:    200,
		RemoteHost:      "5.103.132.56",
		BackendLatency:  10,
		GatewayLatency:  10,
		Source:          "SDK_GOLANG",
		RequestHeaders:  []string{},
		ResponseHeaders: []string{},
		Elements:        []metering.ElementDto{},
	}

	_, _, err := apiClient.MeteringApi.Meter(context.Background(), request)
	if err != nil {
		panic(err)
	}
	println("API request successfully metered")
}
```

## Documentation for API Endpoints

All URIs are relative to *https://api.revenium.io/meter/v1/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*EventsApi* | [**SaveEvent**](docs/EventsApi.md#saveevent) | **Post** /event | Save can API event
*MeteringApi* | [**Meter**](docs/MeteringApi.md#meter) | **Post** /meter | Insert API metering data
*MeteringApi* | [**Valid**](docs/MeteringApi.md#valid) | **Get** /meter/product-key | Determine if a ProductKey is valid or not

## Documentation For Models

 - [ApiEventDto](docs/ApiEventDto.md)
 - [ElementDto](docs/ElementDto.md)
 - [MeteringRequestDto](docs/MeteringRequestDto.md)

## Author

info@revenium.io
