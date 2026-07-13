# Mesh Inspections

Inspections in the **Mesh** category look at topology and transforms. All of them read the object's evaluated mesh (post-modifiers) unless noted otherwise.

## Ngons

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds faces with more than 4 vertices. N-gons can triangulate unpredictably, cause shading artifacts, and often indicate topology that hasn't been cleaned up.

**Overlay:** highlighted faces.

## Tris

**Severity:** :material-alert:{ style="color: #e6a700" } Warning

Finds triangular faces (3 vertices). Not necessarily wrong — tris are sometimes intentional or unavoidable — but worth reviewing if you expect an all-quad mesh for subdivision or retopology work.

**Overlay:** highlighted faces.

## Loose Verts

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds vertices that aren't connected to any edge. These add nothing to the mesh and are usually leftover from deleting geometry.

**Overlay:** vertex markers.

## Non-Manifold

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds edges shared by a number of faces other than 2 (i.e. boundary edges shared by only 1 face, or edges shared by 3+ faces). Non-manifold geometry can break modifiers, booleans, and 3D printing/export pipelines.

**Overlay:** highlighted edges.

## Double Verts

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds vertices within a small merge threshold (`0.0001`, matching Blender's default *Merge by Distance*) of another vertex. Duplicate, coincident vertices usually mean an accidental merge failure or import artifact.

**Overlay:** vertex markers.

## Interior Faces

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds faces where **every** edge is shared by more than 2 faces — geometry buried inside the mesh with no exterior boundary. Common after boolean operations or bad merges.

**Overlay:** highlighted faces.

## Inverted Face

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds faces whose normal disagrees with a neighboring face across a shared edge — a sign the face's winding is flipped relative to the surface around it. Inverted normals cause inside-out shading and lighting errors.

**Overlay:** highlighted faces.

## Unapplied Transform

**Severity:** :material-close-circle:{ style="color: #e0392b" } Error

Finds objects with a rotation or scale that hasn't been applied (i.e. the object's rotation/scale isn't identity). Unapplied transforms can cause inconsistent behavior with modifiers, physics, and exports.

**Overlay:** none — this flags the object as a whole, not specific geometry.

## N Poles

**Severity:** :material-alert:{ style="color: #e6a700" } Warning

Finds vertices connected to 6 or more edges (high valence). High-valence poles tend to cause visible pinching under subdivision.

**Overlay:** vertex markers.
