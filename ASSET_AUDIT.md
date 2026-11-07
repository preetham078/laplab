# Laptop Lab — asset audit

## Current status

No source models, texture sets, HDRIs, or reference photographs are present in
this repository. `index.html` contains a prototype made from Three.js primitive
geometry. It must not be presented as the requested photorealistic product and
will be replaced rather than reused for the production 3D scene.

## Required production assets

All meshes below need to be independently named/selectable GLB files, authored
at 1 unit = 1 cm, PBR textured, and supplied with a license record.

| Asset | File | Required detail / dimensions |
|---|---|---|
| Chassis and bottom cover | `chassis.glb` | 36 × 25 × 2 cm 15.6-inch shell; vents, screw bosses, rubber feet, I/O cut-outs, brushed aluminium textures |
| Lid + hinge | `lid-hinge.glb` | Separate pivoting lid; 0–135° hinge, bezel, webcam, logo/decals |
| IPS display | `display-panel.glb` | 15.6-inch eDP panel, glass/clearcoat, panel texture and emissive screen surface |
| Keyboard / palm rest | `keyboard-palmrest.glb` | Individually shaped keycaps, legends, trackpad aperture, appropriate fasteners |
| Glass trackpad | `trackpad.glb` | Glass layer, chamfer, ribbon connector |
| Motherboard | `motherboard.glb` | 3D board outline, solder mask, copper traces, slots, connectors, silkscreen |
| CPU package | `cpu-bga.glb` | BGA package and heat-spreader engraving; fixed/soldered |
| GPU package | `gpu-bga.glb` | BGA package and heat-spreader engraving; fixed/soldered |
| DDR5 SODIMM | `ram-ddr5-sodimm.glb` | 6.76 × 3.0 cm, edge contacts, chips, label; removable animation origin at connector |
| M.2 2280 NVMe SSD | `ssd-m2-2280.glb` | 8.0 × 2.2 cm, NAND/controller labels, gold connector and retention-hole pivot |
| 2.5-inch HDD | `hdd-2_5in.glb` | 10.0 × 7.0 × 0.7 cm, metal cover, SATA connector, label |
| Battery | `battery-45-99wh.glb` | Pack variants or morphs, rating label, connector, screw mounts |
| Wi-Fi card | `wifi-m2-2230.glb` | 2.23 × 3.0 cm M.2 card, antenna connectors, gold contacts |
| Cooling module | `cooling-module.glb` | Fan housing, blades, copper heat pipes, fin stack, screws; separate named fan/pipe meshes where interaction needs it |
| Speakers | `speaker-pair.glb` | Driver diaphragms, enclosures and cable details |
| Ports daughterboard | `io-ports.glb` | USB-C, USB-A, HDMI, audio and board/cable detail |
| Screws / clips | `fasteners.glb` | Serviceable fasteners and RAM retaining clips required for removal animation |

## Required texture / lighting assets

- 2K/4K PBR texture sets: anodised brushed aluminium, keycaps with legends,
  PCB solder mask + copper/silkscreen, black epoxy IC markings, copper,
  gold contacts, rubber, glass and battery/drive labels.
- One commercial-use HDRI studio environment, plus a real display wallpaper
  whose license permits redistribution.
- Reference photos for the chosen laptop platform: closed exterior, open deck,
  underside and bare internal layout. These establish the real geometry rather
  than a generic collage of parts.

## Source and licensing gates

Before importing, each asset must have a URL, creator, license, modification
record, and any attribution requirement entered in `CREDITS.md`. Allowed
sources are a user-provided asset, a verified CC0/compatible source (for
example Poly Haven for HDRIs), or a commissioned/original Blender model.
Models must be checked for redistribution rights; a view/download page alone
is not proof of permission.

## Missing inputs that determine the result

1. A chosen real laptop platform and its reference photographs, or permission
   to create an original, plausible 15.6-inch reference design.
2. Licensed component GLBs and texture sets, or permission to author all of
   the listed components in Blender and use only self-authored materials.
3. A licensed HDRI/display image (or permission to source verified CC0 assets).

Once those inputs are available, the existing primitive prototype can be
replaced with a model-loading pipeline, component transforms, the disassembly
sequence, and performance/build persistence.
