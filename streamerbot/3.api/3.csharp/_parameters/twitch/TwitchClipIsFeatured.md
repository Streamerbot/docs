---
name: isFeatured
type: Boolean?
default: null
value: true
description: |
  Toggle featured clips behavior

  If the parameter left empty or `null`{lang=cs}, **all** clips will be retrieved, including **both** those flagged as featured, and those not flagged.

  If `isFeatured`{lang=cs} is set to `true`{lang=cs}, then only clips that have `is_featured`{lang=json} set will be retrieved.

  If `isFeatured`{lang=cs} is set to `false`{lang=cs}, then only clips that do not have `is_featured`{lang=json} set will be retrieved.
---