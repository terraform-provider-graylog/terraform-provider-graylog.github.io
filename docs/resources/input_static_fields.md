# graylog_input_static_fields

* [Example](../../examples/v0.12/input.tf)
* [Source Code](../../graylog/resource/system/input/staticfield/resource.go)

## Argument Reference

### Required Argument

name | type
--- | ---
input_id | string

### Optional Argument

name | default | type
--- | --- | ---
fields | | map[string]string

## Import

`graylog_input_static_fields` can be imported using the Input id, e.g.

```console
$ terraform import graylog_input_static_fields.test 5c4acaefc9e77bbbbbbbbbbb
```
