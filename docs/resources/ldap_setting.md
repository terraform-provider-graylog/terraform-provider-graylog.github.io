# graylog_ldap_setting

* [Example](https://github.com/terraform-provider-graylog/terraform-provider-graylog/blob/master/examples/v0.12/ldap_setting.tf)
* [Source Code](https://github.com/terraform-provider-graylog/terraform-provider-graylog/blob/master/graylog/resource/system/ldap/setting/resource.go)

## Argument Reference

### Required Argument

name | example | type
--- | --- | ---
system_username | | string
ldap_uri | "ldap://localhost:389" | string
search_base | | string
search_pattern | | string
display_name_attribute | | string
default_group | | string |

Note that `system_passoword` is optional as Terraform schema but is required to create a LDAP setting.
If we make `system_password` required as Terrafrom schema, we have to store `system_password` in the Terraform state file, which some users wouldn't want it.

### Optional Argument

name | default | type | description
--- | --- | --- | ---
description | "" | string |
enabled | false | bool |
use_start_tls | false | bool |
trust_all_certificates | false | bool |
active_directory | false | bool |
group_search_base | "" | string |
group_id_attribute | "" | string |
group_search_pattern | "" | string |
group_mapping | | map[string]string |
system_password | "" | string | sensitive, computed

## Attributes Reference

name | type
--- | ---
system_password_set | bool

## Import

Unlike other resources, LDAP settings has no id,
so when you import the LDAP settings, please specify some string as id.

```console
$ terraform import graylog_ldap_setting.foo bar
```
