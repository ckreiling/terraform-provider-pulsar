---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "pulsar_namespace Resource - terraform-provider-pulsar"
subcategory: ""
description: |-
  
---

# pulsar_namespace (Resource)





<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `namespace` (String) Pulsar namespaces are logical groupings of topics
- `tenant` (String) An administrative unit for allocating capacity and enforcing an 
authentication/authorization scheme

### Optional

- `backlog_quota` (Block Set) (see [below for nested schema](#nestedblock--backlog_quota))
- `dispatch_rate` (Block Set, Max: 1) Data transfer rate, in and out of the Pulsar Broker (see [below for nested schema](#nestedblock--dispatch_rate))
- `enable_deduplication` (Boolean)
- `namespace_config` (Block Set, Max: 1) (see [below for nested schema](#nestedblock--namespace_config))
- `permission_grant` (Block Set) (see [below for nested schema](#nestedblock--permission_grant))
- `persistence_policies` (Block Set, Max: 1) (see [below for nested schema](#nestedblock--persistence_policies))
- `retention_policies` (Block Set, Max: 1) (see [below for nested schema](#nestedblock--retention_policies))

### Read-Only

- `id` (String) The ID of this resource.

<a id="nestedblock--backlog_quota"></a>
### Nested Schema for `backlog_quota`

Required:

- `limit_bytes` (String)
- `limit_seconds` (String)
- `policy` (String)
- `type` (String)


<a id="nestedblock--dispatch_rate"></a>
### Nested Schema for `dispatch_rate`

Required:

- `dispatch_byte_throttling_rate` (Number)
- `dispatch_msg_throttling_rate` (Number)
- `rate_period_seconds` (Number)


<a id="nestedblock--namespace_config"></a>
### Nested Schema for `namespace_config`

Optional:

- `anti_affinity` (String)
- `is_allow_auto_update_schema` (Boolean)
- `max_consumers_per_subscription` (Number)
- `max_consumers_per_topic` (Number)
- `max_producers_per_topic` (Number)
- `message_ttl_seconds` (Number)
- `replication_clusters` (List of String)
- `schema_compatibility_strategy` (String)
- `schema_validation_enforce` (Boolean)


<a id="nestedblock--permission_grant"></a>
### Nested Schema for `permission_grant`

Required:

- `actions` (Set of String)
- `role` (String)


<a id="nestedblock--persistence_policies"></a>
### Nested Schema for `persistence_policies`

Required:

- `bookkeeper_ack_quorum` (Number)
- `bookkeeper_ensemble` (Number)
- `bookkeeper_write_quorum` (Number)
- `managed_ledger_max_mark_delete_rate` (Number)


<a id="nestedblock--retention_policies"></a>
### Nested Schema for `retention_policies`

Required:

- `retention_minutes` (String)
- `retention_size_in_mb` (String)

