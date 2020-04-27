# graylog_dashboard_widget

* [Example](../../examples/v0.12/dashboard.tf)
* [Source Code](../../graylog/resource/dashboard/widget/resource.go)

## Argument Reference

## Required Argument

name | type
--- | ---
type | string
description | string
dashboard_id | string
configuration | JSON string

## Optional Argument

name | type | default
--- | --- | ---
cache_time | int |

## Attributes Reference

name | type
--- | ---
creator_user_id | string

## Import

`graylog_dashboard_widget` can be imported using `<Dashboard id>/<Widget id>`, e.g.

```console
$ terraform import graylog_dashboard_widget.test 5c4acaefc9e77bbbbbbbbbbb/5c4acaefc9e77bbbbbbbbbbb
```
