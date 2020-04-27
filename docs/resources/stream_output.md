# graylog_stream_output

* [Example](../../examples/v0.12/stream_output.tf)
* [Source Code](../../graylog/resource/stream/output/resource.go)

## Argument Reference

### Required Argument

name | type | etc
--- | --- | ---
stream_id | string | `force new`
output_ids | []string |

#### Note

This resource treats the stream id as the resource id.
So please make the stream id unique in all `graylog_stream_output` resources.

### Optional Argument

None.

## Attributes Reference

None.

## Import

`graylog_stream_output` can be imported using the Stream id, e.g.

```console
$ terraform import graylog_stream_output.test 5c4acaefc9e77bbbbbbbbbbb
```
