# Data source graylog_dashboard

* [Source Code](../../graylog/datasource/dashboard/resource.go)

```tf
data "graylog_dashboard" "test" {
  title = "test"
}
```

## Required Argument

One of `dashboard_id` or `title` must be set.

## Attributes

name | type
--- | ---
title | string
dashboard_id | string
description | string
