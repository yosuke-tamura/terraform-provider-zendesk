---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "zendesk_ticket_form Resource - terraform-provider-zendesk"
subcategory: ""
description: |-
  
---

# zendesk_ticket_form (Resource)



## Example Usage

```terraform
# API reference:
#   https://developer.zendesk.com/rest_api/docs/support/ticket_forms

resource "zendesk_ticket_form" "form-1" {
  name = "Form 1"
  ticket_field_ids = [
    data.zendesk_ticket_field.assignee.id,
    data.zendesk_ticket_field.description.id,
    data.zendesk_ticket_field.group.id,
    data.zendesk_ticket_field.status.id,
    data.zendesk_ticket_field.subject.id,
    zendesk_ticket_field.checkbox-field.id,
    zendesk_ticket_field.date-field.id,
    zendesk_ticket_field.decimal-field.id,
    zendesk_ticket_field.integer-field.id,
  ]
}

resource "zendesk_ticket_form" "form-2" {
  name = "Form 2"
  ticket_field_ids = [
    data.zendesk_ticket_field.assignee.id,
    data.zendesk_ticket_field.description.id,
    data.zendesk_ticket_field.group.id,
    data.zendesk_ticket_field.status.id,
    data.zendesk_ticket_field.subject.id,
    zendesk_ticket_field.regexp-field.id,
    zendesk_ticket_field.tagger-field.id,
    zendesk_ticket_field.text-field.id,
    zendesk_ticket_field.textarea-field.id,
  ]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String)

### Optional

- `active` (Boolean)
- `default` (Boolean)
- `display_name` (String)
- `end_user_visible` (Boolean)
- `id` (String) The ID of this resource.
- `in_all_brands` (Boolean)
- `position` (Number)
- `ticket_field_ids` (Set of Number)

### Read-Only

- `restricted_brand_ids` (Set of Number)
- `url` (String)


