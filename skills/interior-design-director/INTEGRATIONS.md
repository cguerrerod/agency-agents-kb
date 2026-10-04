# Interior Design Director — Technical Integration Map

These integrations are optional capability layers. The skill should remain useful without them.

## Tier 1 — Core AEC geometry

### IfcOpenShell / Bonsai
Use for:
- IFC ingestion;
- spaces, walls, doors, windows and storeys;
- BIM semantics;
- geometry extraction and validation.

### FreeCAD + FreeCAD MCP
Use for:
- dimensioned parametric geometry;
- 2D sketches and 3D solids;
- repeatable layout constraints;
- measured CAD outputs.

### COMPAS
Use for:
- geometry calculations;
- computational design;
- data structures and AEC geometry operations.

## Tier 2 — Visual / reality understanding

### Depth Anything V2
Use for relative depth cues from a single image.
Never treat monocular relative depth as metric measurement without calibration.

### SAM 2
Use for object/region segmentation in images and video.

### COLMAP
Use when multiple overlapping photographs are available for multi-view reconstruction.

### Open3D
Use for point clouds, registration, surface reconstruction and 3D processing.

### CubiCasa5K-derived methods
Use as a reference/dataset family for semantic floor-plan recognition. Validate against current implementations before deployment.

## Tier 3 — Visualization

### Blender + MCP for Blender
Use for:
- scene assembly;
- furniture massing;
- materials/lighting;
- camera-consistent visual alternatives.

Conceptual renders must not be presented as construction drawings.

## Tier 4 — Environmental analysis

### Ladybug / Honeybee
Use for:
- sun/daylight studies;
- energy-related building representations;
- environmental performance.

Requires reliable geometry/orientation for meaningful results.

## Tier 5 — Interoperability

### Speckle
Use as an AEC data exchange layer when models need to move among tools or collaborators.

## Structural analysis

### PyNite
May support preliminary engineering reasoning for simple models. It does not replace professional structural engineering review or stamped calculations.

## Integration principle
External engines calculate or transform evidence. The Interior Design Director remains responsible for:
- evidence certainty;
- design intent;
- specialist routing;
- conflict resolution;
- human-readable recommendation;
- escalation boundaries.
