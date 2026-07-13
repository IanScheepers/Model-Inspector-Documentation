# UV Inspections

Inspections in the **UV** category look at the object's active UV map.

## Missing UV Map

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds meshes that have faces but no UV layer at all. Without UVs, texturing and baking aren't possible.

**Overlay:** none — this flags the object as a whole.

## Too Many UV Maps

**Severity:** :material-alert:{ style="color: #e6a700" } Warning

Finds meshes with more than one UV map. Extra, unused UV maps bloat file size and can cause confusion about which map is actually used for texturing/baking.

**Overlay:** none — the count shown is the number of UV maps present.

## Overlapping UVs

**Severity:** :material-alert:{ style="color: #e6a700" } Warning

Finds faces whose UV islands overlap another face's UVs (excluding triangles that belong to the same n-gon). Overlapping UVs are sometimes intentional (tiling/mirrored islands) but can cause unwanted texture bleed when baking.

**Overlay:** highlighted faces.

## Zero Area UVs

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds faces collapsed to zero or near-zero area in UV space. A face with no UV area can't display a texture correctly.

**Overlay:** highlighted faces.

## UVs Out of 0-1 Bounds

**Severity:** :material-alert:{ style="color: #e6a700" } Warning

Finds faces with UV coordinates outside the standard 0–1 tile. Sometimes intentional (UDIMs, tiling), but often means the UVs need to be packed.

**Overlay:** highlighted faces.
