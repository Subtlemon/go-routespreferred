# Google Maps Platform Routes Preferred API Client for Go

[![Test](https://github.com/googlemaps/go-routespreferred/workflows/Test/badge.svg)][test]
[![Release](https://github.com/googlemaps/go-routespreferred/workflows/Release/badge.svg)][release]
[![Generation](https://github.com/googlemaps/go-routespreferred/workflows/Generation/badge.svg)][generation]
[![codecov](https://codecov.io/gh/googlemaps/go-routespreferred/branch/master/graph/badge.svg)](https://codecov.io/gh/googlemaps/go-routespreferred)
[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)

Go idiomatic client for Google Maps Platform Routes PreferredAPI.

> **NOTE:** The libraries in this repository should be considered experimental at this time and breaking changes should be expected.

> **NOTE:** The libraries in this repository are [autogenerated][generation] from the interface definitions in the [googleapis/googleapis repository][googleapis] using [Bazel][bazel].

## Installation

`go get developers.google.com/maps/go/routespreferred`

## Requirements

### Create a Project

You will need a [Google Cloud Platform][developer-console] project. [Follow these instructions][create-project] to get your project set up.

### Enable the Routes Preferred API
You will need to [enable][enable-api] the Google Maps Platform Routes PreferredAPI.

[![](https://img.shields.io/badge/Enable%20API-Routes%20Preferred-important)][enable-api]

### Enable billing
You will need to [enable billing][enable-billing] to use the Google Maps Platform Routes API.

### Local development environment
You will need to set up the local development environment. 

Get started quickly by [installing the Google Cloud SDK][cloud-sdk] and running the following commands in command line:
  `gcloud auth login` and `gcloud config set project [YOUR PROJECT ID]`.

## Authentication

Routes Preferred supports authentication by OAuth token, self-signed JWT, and API Key. This library only supports OAuth and JWT from service account credentials. You can specify OAuth with `option.WithScopes("https://www.googleapis.com/auth/maps-platform.routespreferred")` or JWT with `option.WithAudiences("https://routespreferred.googleapis.com/")`, though these are both set by default.

To run outside of App Engine/Compute Engine environments, download service account credentials following [these instructions](https://cloud.google.com/iam/docs/creating-managing-service-account-keys#creating_service_account_keys) and point to it with `option.WithCredentialsFile(...)` or the `GOOGLE_APPLICATION_CREDENTIALS` environment variable. See the [compute routes sample](https://github.com/googlemaps/go-routespreferred/blob/master/samples/compute-routes/main.go) for a complete example.

App Engine/Compute Engine instances are associated with a default service account, which this library will use by default to authenticate. However, since Routes Preferred isn't a Cloud API, the `cloud-platform` scope will not grant access to it. [Follow these instructions](https://cloud.google.com/compute/docs/access/create-enable-service-accounts-for-instances#changeserviceaccountandscopes) to set the `https://www.googleapis.com/auth/maps-platform.routespreferred` scope for your instance. Note that the scope doesn't appear on the Cloud Console, so you should use the `gcloud` command line interface.

## Transport

Google Maps Platform Routes Preferred API uses [gRPC][grpc] for the transport layer.

## Versioning

This library follows [Semantic Versioning](http://semver.org/).

## Contributing

Contributions to this library are always welcome and highly encouraged.

See [CONTRIBUTING][contributing] for more information how to get started.

## License

Apache 2.0 - See [LICENSE][license] for more information.

[authentication]: https://github.com/googleapis/google-cloud-go#authentication
[developer-console]: https://console.developers.google.com/
[create-project]: https://cloud.google.com/resource-manager/docs/creating-managing-projects
[cloud-sdk]: https://cloud.google.com/sdk/
[contributing]: https://github.com/googlemaps/go-routespreferred/blob/master/CONTRIBUTING.md
[license]: https://github.com/googlemaps/go-routespreferred/blob/master/LICENSE
[release]: https://github.com/googlemaps/go-routespreferred/actions?query=workflow%3ARelease
[test]: https://github.com/googlemaps/go-routespreferred/actions?query=workflow%3ATest
[generation]: https://github.com/googlemaps/go-routespreferred/actions?query=workflow%3AGeneration
[enable-billing]: https://cloud.google.com/apis/docs/getting-started#enabling_billing
[enable-api]: https://console.cloud.google.com/flows/enableapi?apiid=routespreferred.googleapis.com
[grpc]: https://grpc.io/
[googleapis]: https://github.com/googleapis/googleapis
[bazel]: https://bazel.build
