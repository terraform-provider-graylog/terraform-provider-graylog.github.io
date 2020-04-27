# graylog_pipeline

* [Example](../../examples/v0.12/pipeline.tf)
* [Source Code](../../graylog/resource/system/pipeline/pipeline/resource.go)

## Argument Reference

### Required Argument

name | type | etc
--- | --- | ---
source | string |

### Optional Argument

name | default | type | etc
--- | --- | --- | ---
description | string |

## Attributes Reference

Nothing.

## Import

`graylog_pipeline` can be imported using the Pipeline id, e.g.

```console
$ terraform import graylog_pipeline.test 5c4acaefc9e77bbbbbbbbbbb
```
