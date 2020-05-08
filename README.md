# terraform-provider-graylog

[![Build Status](https://github.com/terraform-provider-graylog/terraform-provider-graylog/workflows/CI/badge.svg)](https://github.com/terraform-provider-graylog/terraform-provider-graylog/actions)
[![codecov](https://codecov.io/gh/terraform-provider-graylog/terraform-provider-graylog/branch/master/graph/badge.svg)](https://codecov.io/gh/terraform-provider-graylog/terraform-provider-graylog)
[![Go Report Card](https://goreportcard.com/badge/github.com/terraform-provider-graylog/terraform-provider-graylog)](https://goreportcard.com/report/github.com/terraform-provider-graylog/terraform-provider-graylog)
[![GitHub last commit](https://img.shields.io/github/last-commit/terraform-provider-graylog/terraform-provider-graylog.svg)](https://github.com/terraform-provider-graylog/terraform-provider-graylog)
[![License](https://img.shields.io/badge/license-mit-blue.svg?style=flat-square)](https://raw.githubusercontent.com/terraform-provider-graylog/terraform-provider-graylog/master/LICENSE)

Document of [terraform-provider-graylog](https://github.com/terraform-provider-graylog/terraform-provider-graylog)

## What's terraform-provider-graylog?

terraform-provider-graylog is a [Terraform](https://www.terraform.io/) provider for [Graylog](https://docs.graylog.org/).

Using this provider, we can manage Graylog's various resources with Terraform.

## Example Usage

```tf
# Configure Graylog Provider
provider "graylog" {
  web_endpoint_uri = "http://example.com/api"
  api_version      = "v3"
}

# Create a Input
resource "graylog_input" "gelf_udp" {
  title  = "gelf udp"
  type   = "org.graylog2.inputs.gelf.udp.GELFUDPInput"
  global = true

  attributes = jsonencode({
    bind_address          = "0.0.0.0"
    port                  = 12201
    recv_buffer_size      = 262144
    decompress_size_limit = 8388608
  })
}
```

About Provider's configuration, please see [Provider Configuration](provider.md).

Please see [example](https://github.com/terraform-provider-graylog/terraform-provider-graylog/tree/master/examples/v0.12) also.

## Install

[Download binary](https://github.com/terraform-provider-graylog/terraform-provider-graylog/releases) and install it.

https://www.terraform.io/docs/configuration/providers.html#third-party-plugins

## Relation to go-graylog

We originally developed [go-graylog](https://github.com/suzuki-shunsuke/go-graylog), which provides Go's API client and Terraform provider for Graylog.  
But at go-graylog there are some structural challenges and it is difficult to support Graylog's complicated and undocumented API.  
So we decided to develop a new provider from scratch as the successor of go-graylog.

This provider supports all resources which are supported by go-graylog.  
Unfortunately there are some breaking changes and we have to fix Terraform configuration (.tf files) manually to migrate from go-graylog.

For detail, please see the following pages.

* [What is changed from go-graylog?](migration/what-is-changed.md)
* [Migration Guide Overview](migration/guide.md)
* [Migration Guide Detail](migration/detail.md)
