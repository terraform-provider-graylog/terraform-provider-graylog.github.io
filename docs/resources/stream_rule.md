# graylog_stream_rule

* [Example](../../examples/v0.12/stream_rule.tf)
* [Source Code](../../graylog/resource/stream/rule/resource.go)

## Argument Reference

### Required Argument

name | type
--- | ---
field | string
value | string
description | string
type | int
stream_id | string

### Optional Argument

name | default | type
--- | --- | ---
inverted | | bool

## Attributes Reference

name | type
--- | ---
rule_id | string

## Import

`graylog_stream_rule` can be imported using `<stream id/stream rule id>`, e.g.

```console
$ terraform import graylog_stream_rule.test 5bb1b4b5c9e77bbbbbbbbbbb/5c4acaefc9e77bbbbbbbbbbb
```
