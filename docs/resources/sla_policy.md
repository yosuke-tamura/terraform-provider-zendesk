---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "zendesk_sla_policy Resource - terraform-provider-zendesk"
subcategory: ""
description: |-
  
---

# zendesk_sla_policy (Resource)



## Example Usage

```terraform
# API reference:
#   https://developer.zendesk.com/rest_api/docs/support/sla_policies

resource "zendesk_sla_policy" "incidents_sla_policy" {
  title  = "Incidents"
  active = true

  all {
    field    = "type"
    operator = "is"
    value    = "incident"
  }

  policy_metrics {
    priority = "normal"
    metric = "first_reply_time"
    target = 30
    business_hours = false
  }
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `policy_metrics` (Block Set, Min: 1) (see [below for nested schema](#nestedblock--policy_metrics))
- `title` (String)

### Optional

- `active` (Boolean)
- `all` (Block Set) (see [below for nested schema](#nestedblock--all))
- `any` (Block Set) (see [below for nested schema](#nestedblock--any))
- `description` (String)
- `id` (String) The ID of this resource.

### Read-Only

- `position` (Number)

<a id="nestedblock--policy_metrics"></a>
### Nested Schema for `policy_metrics`

Required:

- `metric` (String)
- `priority` (String)
- `target` (Number)

Optional:

- `business_hours` (Boolean)


<a id="nestedblock--all"></a>
### Nested Schema for `all`

Required:

- `field` (String)
- `operator` (String)
- `value` (String)


<a id="nestedblock--any"></a>
### Nested Schema for `any`

Required:

- `field` (String)
- `operator` (String)
- `value` (String)

