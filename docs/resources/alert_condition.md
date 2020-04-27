# graylog_alert_condition

* [Example](../../examples/v0.12/alert_condition.tf)
* [Source Code](../../graylog/resource/stream/alert/condition/resource.go)

## Argument Reference

### Required Argument

name | type
--- | ---
stream_id | string
type | string
title | string
parameters | JSON string

### Optional Argument

name | default | type
--- | --- | ---
in_grace | false | bool

### parameters

`parameters` is a JSON string whose type is `object`.
The data structure of JSON is different per AlertCondition `type`.
Please see the [example](../../examples/v0.12/alert_condition.tf).

### Attributes Reference

name | type
--- | ---
alert_condition_id | string

## Import

`graylog_alert_condition` can be imported using the User `<stream id>/<alert condition id>`, e.g.

```console
$ terraform import graylog_alert_condition.test 5bb1b4b5c9e77bbbbbbbbbbb/5c4acaefc9e77bbbbbbbbbbb
```
