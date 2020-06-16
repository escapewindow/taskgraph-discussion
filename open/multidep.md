# Multidep loader

- The `multi_dep` loader can probably obsolete the `single_dep` loader, if we had a `group_by: label`.
- We may be able to genericize our `group_by` logic to allow for, say, `group_by: ['attributes.build_platform', 'attributes.build_type', 'attributes.shipping_product']`
  - The current `group_by: platform` also looks at `task.shipping-product`; we would need to standardize on the attribute if we went this route
- The skeleton of `multi_dep` could then be generic enough to land in standalone taskgraph.
