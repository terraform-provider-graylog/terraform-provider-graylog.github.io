# Data source graylog_sidecar

* [Source Code](https://github.com/terraform-provider-graylog/terraform-provider-graylog/blob/master/graylog/datasource/sidecar/data_source.go)

```tf
data "graylog_sidecar" "test" {
  node_name = "test"
}
```

## Required Argument

One of `node_id` or `node_name` must be set.

## Attributes

name | type
--- | ---
node_id | string
node_name | string
