---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "zendesk_brand Resource - terraform-provider-zendesk"
subcategory: ""
description: |-
  
---

# zendesk_brand (Resource)



## Example Usage

```terraform
# API reference:
#   https://developer.zendesk.com/rest_api/docs/support/brands

resource "zendesk_brand" "T-800" {
  name            = "T-800"
  active          = true
  subdomain       = "d3v-terraform-provider-t800"
  # TODO: logo
}

resource "zendesk_brand" "T-1000" {
  name            = "T-1000"
  active          = false
  subdomain       = "d3v-terraform-provider-t1000"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String)
- `subdomain` (String)

### Optional

- `active` (Boolean)
- `default` (Boolean)
- `host_mapping` (String)
- `id` (String) The ID of this resource.
- `logo_attachment_id` (Number)
- `signature_template` (String)

### Read-Only

- `brand_url` (String)
- `has_help_center` (Boolean)
- `help_center_state` (String)
- `ticket_form_ids` (Set of Number)
- `url` (String)


