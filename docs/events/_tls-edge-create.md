| &nbsp; | &nbsp; | &nbsp; |
|---|---|---|
| description | string | human-readable description of what this edge will be used for; optional, max 255 bytes. |
| metadata | string | arbitrary user-defined machine-readable data of this edge. Optional, max 4096 bytes. |
| hostports | List&lt;string&gt; | hostports served by this edge |
| enabled | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| backend_id | string | backend to be used to back this endpoint |
| enabled | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| ip_policy_ids | List&lt;string&gt; | list of all IP policies that will be used to check if a source IP is allowed access to the endpoint |
| enabled | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| certificate_authority_ids | List&lt;string&gt; | list of certificate authorities that will be used to validate the TLS client certificate presented by the initiator of the TLS connection |
| enabled | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| terminate_at | string | `edge` if the ngrok edge should terminate TLS traffic, `upstream` if TLS traffic should be passed through to the upstream ngrok agent / application server for termination. if `upstream` is chosen, most other modules will be disallowed because they rely on the ngrok edge being able to access the underlying traffic. |
| min_version | string | The minimum TLS version used for termination and advertised to the client during the TLS handshake. if unspecified, ngrok will choose an industry-safe default. This value must be null if `terminate_at` is set to `upstream`. |