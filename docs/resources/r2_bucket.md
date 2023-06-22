---
page_title: "cloudflare_r2_bucket Resource - Cloudflare"
subcategory: ""
description: |-
  The R2 Bucket https://developers.cloudflare.com/r2/ resource allows you to manage Cloudflare R2 buckets.
---

# cloudflare_r2_bucket (Resource)

## Example Usage

```terraform
resource "cloudflare_r2_bucket" "example" {
  account_id = "f037e56e89293a057740de681ac9abbe"
  name       = "terraform-bucket"
  location   = "enam"
}
```

-> Available location values can be found in the [R2 documentation](https://developers.cloudflare.com/r2/buckets/data-location/#available-hints).


<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `account_id` (String) The account identifier to target for the resource.
- `name` (String) The name of the R2 bucket.

### Optional

- `location` (String) The location hint of the R2 bucket.

### Read-Only

- `id` (String) The identifier of this resource.

## Import

Import is supported using the following syntax:

```shell
$ terraform import cloudflare_r2_bucket.default <account id>/<bucket name>
```