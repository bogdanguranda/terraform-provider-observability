---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "observability_object Resource - observability"
subcategory: ""
description: |-
  Object resource
---

# observability_object (Resource)

Object resource

Enables you to create and manage any object of Cisco Observability Platform. Objects are actual populated values of a type. Data is a field which acts like a container for any object payload.

## Example usage

```terraform
resource "observability_object" "conn" {
  type_name  = "<your type>"
  object_id  = "<object id of the object>"
  layer_type = "TENANT"
  layer_id   = "<your tenant>"
  import_id  = "<object type>|<object id>|TENANT|<your tenant>"
  data = jsonencode(
    {
      "field1" : "value1",
      "field2" : "value2",
      ...
    }
  )
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `layer_id` (String) Specifies the layer ID where the object resides
- `layer_type` (String) Specifies the layer type where the object resides
- `type_name` (String) Specifies the fully qualified type name used to get the type

### Optional

- `data` (String) JSON schema of the returned object
- `import_id` (String) ID used when doing import operation on an object
- `object_id` (String) Spepcified the object ID for the particular object to get

### Read-Only

- `id` (String) Used to provide compatibility for testing framework
