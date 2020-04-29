# Provider Configuration

## Variables

### Required Variables

name | Environment variable | description
--- | --- | ---
web_endpoint_uri | GRAYLOG_WEB_ENDPOINT_URI | API endpoint, for example https://example.com/api
auth_name | GRAYLOG_AUTH_NAME | Username or API token or Session Token
auth_password | GRAYLOG_AUTH_PASSWORD | Password or the literal `"token"` or `"session"`

About `auth_name` and `auth_password`, please see the [Graylog's Documentation](https://docs.graylog.org/en/latest/pages/configuration/rest_api.html).

You can authenticate with either password or access token or session token.

password

```
auth_name = "<user name>"
auth_password = "<password>"
```

access token

```
auth_name = "<access token>"
auth_password = "token"
```

session token

```
auth_name = "<session token>"
auth_password = "session"
```

### Optional

name | Environment variable | default | description
--- | --- | --- | ---
x_requested_by | GRAYLOG_X_REQUESTED_BY | terraform-go-graylog | [X-Requested-By Header](https://github.com/Graylog2/graylog2-server/blob/370dd700bc8ada5448bf66459dec9a85fcd22d58/UPGRADING.rst#protecting-against-csrf-http-header-required)
api_version | GRAYLOG_API_VERSION | "v3" | Graylog's API version
