
# 3D Models

This directory contains the STL enclosure components for the Memory Sequence Game.

## Model Files

| File | Description |
|---|---|
| `memory-game-base.stl` | Main enclosure base for housing the electronics. |
| `memory-game-lid.stl` | Enclosure lid / upper housing component. |

## Intended Use

The models support the physical assembly of the Arduino-based memory game.

Import the STL files into a slicer or compatible CAD application to inspect, orient, and prepare them for fabrication.

## Recommended Workflow

1. Open each STL in your preferred slicer or CAD software.
2. Confirm the imported units and overall dimensions.
3. Check that the model scale matches the physical build.
4. Inspect button, LED, buzzer, board, cable, and USB clearances.
5. Choose a suitable print orientation and profile.
6. Print a fit-check prototype.
7. Test the lid-to-base fit.

## Important Notes

- STL files contain mesh geometry, not editable parametric design history.
- Printer, filament, layer height, infill, and support settings depend on your equipment.
- Verify component clearances before printing.
- Check access to the USB connector and internal wiring.

## Related Documentation

- [Hardware Guide](../docs/HARDWARE.md)
- [Build Guide](../docs/BUILD_GUIDE.md)
- [Pinout Reference](../docs/PINOUT.md)
