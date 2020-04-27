# graylog_pipeline_connection

* [Example](../../examples/v0.12/pipeline.tf)
* [Source Code](../../graylog/resource/system/pipeline/connection/resource.go)

## Argument Reference

### Required Argument

name | type
--- | ---
stream_id | string
pipeline_ids | []string

#### Note

This resource treats the stream id as the resource id,
because there is no Graylog API to operate resource by connection pipeline id.
So please make the stream id unique in all `graylog_pipeline_connection` resources.

### Optional Argument

None.

## Attributes Reference

Nothing.

## Import

`graylog_pipeline_connection` can be imported using the Stream id, e.g.

```console
$ terraform import graylog_pipeline_connection.test <stream id>
```
