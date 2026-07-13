# Model Inspector

**Model Inspector** is a Blender add-on that validates meshes, UVs, and materials for a set of common modeling mistakes, right inside the 3D Viewport.

Run a set of checks against any object and provides feedback for each test and category as a pass/warning/error breakdown. You can jump straight to the problem geometry with a single click! No more hunting for mystery errors in you models.

<div class="grid cards" markdown>

-   :material-rocket-launch-outline:{ .lg .middle } **New to Model Inspector?**

    ---

    Install the add-on and run your first inspection in a few minutes.

    [:octicons-arrow-right-24: Getting started](getting-started/installation.md)

-   :material-cog-outline:{ .lg .middle } **Learn the workflow**

    ---

    Understand the panel, target object list, and how overlays work.

    [:octicons-arrow-right-24: User guide](user-guide/interface-overview.md)

-   :material-format-list-checks:{ .lg .middle } **Every inspection, explained**

    ---

    Look up exactly what an inspection checks and why it matters.

    [:octicons-arrow-right-24: Inspections reference](inspections/mesh-inspections.md)


</div>

## Why Use Model Inspector?

Modeling mistakes are easy to make and easy to miss. N-gons buried in a dense meshs, UV islands that drifted out of bounds, a material slots that get left empty after a merge. Model Inspector catches these before they turn into a rendering bug, a broken bake, or a rejected asset.

- **Three check categories** — (**Mesh, UV, and Material**) — each with its own set of targeted inspections.
- **Per-object results** — inspect a single object or a whole batch, and see results broken down individually.
- **Visual overlays** — click a flagged result to highlight the exact faces, vertices, or edges in the viewport, color-coded by severity.
- **Non-destructive** — Model Inspector only reads your scene. It never modifies geometry, UVs, or materials.

## Requirements

- Blender **4.2** or newer (Model Inspector ships as a Blender extension).

## What gets checked

| Category | Checks |
| --- | --- |
| [Mesh](inspections/mesh-inspections.md) | Ngons, tris, loose vertices, non-manifold edges, doubles, interior faces, inverted normals, unapplied transforms, high-valence vertices |
| [UV](inspections/uv-inspections.md) | Missing UV maps, too many UV maps, overlapping UVs, zero-area UVs, UVs outside 0–1 bounds |
| [Material](inspections/material-inspections.md) | Missing materials, empty material slots, faces with no material, missing image textures, duplicate materials |

Ready to get started? Head to the [installation guide](getting-started/installation.md).
