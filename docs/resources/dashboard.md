# graylog_dashboard

* [Example](../../examples/v0.12/dashboard.tf)
* [Source Code](../../graylog/resource/dashboard/resource.go)

## Argument Reference

### Required Argument

name | type
--- | ---
title | string
description | string

### Optional Argument

None

## Attrs Reference

name | type
--- | ---
created_at | string

## Import

`graylog_dashboard` can be imported using the Dashboard id, e.g.

```console
$ terraform import graylog_dashboard.test 5c4acaefc9e77bbbbbbbbbbb
```
