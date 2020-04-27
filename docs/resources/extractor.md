# graylog_extractor

* [Example](../../examples/v0.12/extractor.tf)
* [Source Code](../../graylog/resource/system/input/extractor/resource.go)

## Argument Reference

### Required Argument

name | type
--- | ---
input_id | string
type | string
title | string
cursor_strategy
source_field | string
condition_type | string
extractor_config | JSON string
converters[].type | string
converters[].config | JSON string

### Optional Argument

name | type | default
--- | --- | ---
converters | list | []
target_field | string | ""
condition_value | string | ""
order | int | 0

### Attributes Reference

name | type
--- | ---
extractor_id | string

## Import

`graylog_extractor` can be imported using the User `<input id>/<extractor id>`, e.g.

```console
$ terraform import graylog_extractor.test 5bb1b4b5c9e77bbbbbbbbbbb/5c4acaefc9e77bbbbbbbbbbb
```
